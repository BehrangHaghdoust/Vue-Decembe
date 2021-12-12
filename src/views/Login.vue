<template>
  <div class="Login">
    <div class="row">
      <div class="col-lg-4 mx-auto border shadow rounded p-4">
        <h1 class="text-center mt-3 mb-4">Login</h1>
        <form @submit.prevent="doLogin">
          <div class="form-group">
            <label for="usernameInput">Username</label>
            <input type="text" class="form-control" id="usernameInput" v-model="username"/>
          </div>
          <div class="form-group">
            <label for="passwordInput">Password</label>
            <input type="password" class="form-control" id="passwordInput" v-model="password" />
          </div>

          <button type="submit" class="btn btn-primary mt-3">Login</button>
        </form>
      </div>
    </div>
  </div>
</template>


<script>

export default {
  name: 'Login',
  data(){
      return{
          username : '',
          password : ''
      }
  },

  methods :{
      doLogin(){
        //   this.$store.commit("login" , "abc1453")
        //   this.$router.push("/Profile")
        console.log(
            this.username
        )
           console.log(
            this.password
        )
      }
  }

}
</script>