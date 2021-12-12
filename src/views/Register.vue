<template>
  <div class="Register">
    <div class="row">
      <div class="col-lg-4 mx-auto border shadow rounded p-4">
        <h1 class="text-center mt-3 mb-4">Register</h1>
        <form @submit.prevent="doRegister">
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
              {{ usernameEM }}
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
              {{ passwordEM }}
            </div>
          </div>

          <div class="form-group">
            <label for="passwordInput">Repeat Password</label>
            <input
              type="password"
              class="form-control"
              id="passwordInput2"
              v-model="password2"
              :class="{
                'is-invalid': password2E === true,
                'is-valid': password2E === false,
              }"
            />
            <div class="invalid-feedback" v-if="password2E">
              {{ password2EM }}
            </div>
          </div>

          <button type="submit" class="btn btn-primary mt-3">Register</button>
        </form>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Register",
  data() {
    return {
      username: "",
      password: "",
      password2: "",
      usernameE: null,
      passwordE: null,
      password2E: null,
      usernameEM: null,
      passwordEM: null,
      password2EM: null,
    };
  },

  methods: {
    doRegister() {
      let access = true;
      if (this.username.length < 5) {
        if (this.username.length == 0) {
          this.usernameE = true;
          access = false;
          this.usernameEM = "Please enter your user name";
        } else {
          this.usernameEM = "Username must be at least 5 chracter long.";
        }
      } else {
        this.usernameE = false;
        this.usernameEM = "";
      }

      if (this.password.length < 6) {
        access = false;
        if (this.password.length == 0) {
          this.passwordE = true;
          access = false;
          this.passwordEM = "Please enter your password";
        } else {
          this.passwordEM = "Password must be at least 6 chracters long.";
        }
      } else {
        this.passwordE = false;
        this.passwordEM = "";
      }
      // ------------------------part Repeat--------------------------------

      if (this.password2.length < 6) {
        access = false;
        this.password2E = true;

        if (this.password2.length == 0) {
          this.password2EM = "Repeat password required";
        } else {
          this.password2EM = "Repeat password must be at least 6 chracters long.";
        }
      } else {
        this.password2E = false;
        this.password2EM = "";
      }

      if (this.password != this.password2) {
        access = false;
        this.passwordE = true;
        this.password2E = true;
        this.passwordEM = "password aren't same !";
      } else {
        if (!this.passwordEM && !!this.password2EM) {
          this.passwordEM = "";
        }
      }

      if (access) {
        this.$store.commit("login", `${this.username} : ${this.password}`);
        this.$router.push("/Profile");
      }
    },
  },
};
</script>

//  in order to be better for Register/login search :"vuejs password strength"