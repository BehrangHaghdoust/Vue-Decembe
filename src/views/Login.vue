<template>
    <div class="Login">
<button class="btn btn-success" @click="doLogin">Login</button>
    </div>
</template>


<script>

export default {
  name: 'Login',

  methods :{
      doLogin(){
          this.$store.commit("login" , "abc1453")
      }
  }

}
</script>