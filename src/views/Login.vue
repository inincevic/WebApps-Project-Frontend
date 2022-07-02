<template>
  <div class="about">
    <h1 class="title_text">Log in using your credentials</h1>
    <br />
    <br />
    <div class="container">
      <div class="row">
        <div class="col-sm"></div>
        <div class="col-sm">
          <form @submit="checkCredentials()" action="#" onsubmit="return false">
            <div class="form-group">
              <label for="exampleInputEmail1" class="plain_text"
                >Email address</label
              >
              <input
                type="email"
                class="form-control"
                id="exampleInputEmail1"
                aria-describedby="emailHelp"
                placeholder="Enter email"
                v-model="loginCredentials.email"
              />
            </div>
            <div class="form-group">
              <label for="exampleInputPassword1" class="plain_text"
                >Password</label
              >
              <input
                type="password"
                class="form-control"
                id="exampleInputPassword1"
                placeholder="Password"
                v-model="loginCredentials.password"
              />
            </div>
            <button type="submit" class="btn btn-primary">Submit</button>
          </form>
        </div>
        <div class="col-sm"></div>
      </div>
    </div>
  </div>
</template>

<script>

import axios from "axios";

export default {
  name: "Login",

  async mounted() {},

  methods: {
    checkCredentials() {
      axios
        .post("http://localhost:3000/login", this.loginCredentials)
        .then((response) => {
          console.log(response);
          if (response.data) {
            console.log(response.data)
            this.$router.push({
              name: "profile",
            });
          }
          else {
            alert("Incorrect credentials. Please try again. If you are not a user, please register.");
          }
        });
    },
  },

  data() {
    return {
      validLogin: 0,

      loginCredentials: {
        email: "",
        password: "",
      },
    };
  },
};
</script>

<style scoped>
@import url("http://fonts.cdnfonts.com/css/pokemon-solid"); /* font-family: 'Pokemon Solid', sans-serif; */
@import url("http://fonts.cdnfonts.com/css/pokemon-hollow"); /* font-family: 'Pokemon Hollow', sans-serif; */
@import url(//db.onlinewebfonts.com/c/6120639772c6c60a2fad6742051c6feb?family=Unown);

.title_text {
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 75px;
}

.plain_text {
  color: black;
  font-family: "Unown", sans-serif;
  font-size: 35px;
}
</style>
