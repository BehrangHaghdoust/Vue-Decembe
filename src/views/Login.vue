<template>
  <div class="Login">
    <div class="row">
      <div class="col-lg-4 mx-auto border shadow rounded p-4">
        <h1 class="text-center mt-3 mb-4">Login</h1>
        <form @submit.prevent="doLogin">
          <div class="form-group">
            <label for="usernameInput">Username</label>
            <input
              type="text"
              class="form-control"
              id="usernameInput"
              v-model="username"
              :class="{
                'is-invalid': usernameE === true,
                'is-valid': usernameE === false,
              }"
            />
            <div class="invalid-feedback" v-if="usernameE">
              {{usernameEM}}
            </div>
          </div>
          <div class="form-group">
            <label for="passwordInput">Password</label>
            <input
              type="password"
              class="form-control"
              id="passwordInput"
              v-model="password"
              :class="{
                'is-invalid': passwordE === true,
                'is-valid': passwordE === false,
              }"
            />
            <div class="invalid-feedback" v-if="passwordE">
              {{passwordEM}}
            </div>
          </div>

          <button type="submit" class="btn btn-primary mt-3">Login</button>
        </form>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Login",
  data() {
    return {
      username: "",
      password: "",
      usernameE: null,
      passwordE: null,
      usernameEM: null,
      passwordEM: null,
    };
  },

  methods: {
    doLogin() {
let access = true
      if (this.username.length < 5) {
        if (this.username.length == 0) {
          this.usernameE = true;
          access = false
          this.usernameEM = "Please enter your user name";
        } else {
          this.usernameEM = "Username must be at least 5 chracter long.";
        }
      } else {
        this.usernameE = false;
        this.usernameEM = "";
      }

      if (this.password.length < 6) {
           access = false
        if (this.password.length == 0) {
          this.passwordE = true;
          access = false
          this.passwordEM = "Please enter your password";
        } else {
          this.passwordEM = "Password must be at least 6 chracter long.";
        }
      } else {
        this.passwordE = false;
        this.passwordEM = "";
      }
      if(access){
         this.$store.commit("login" , `${this.username} : ${this.password}`)
        this.$router.push("/Profile")
      }

    },
  },
};
</script>