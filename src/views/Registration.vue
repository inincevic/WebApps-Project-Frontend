<template>
  <div class="registration">
    <h1 class="title_text">This is the sign up page</h1>
    <br>
    <br>
    <div class="container">
      <div class="row">
        <div class="col-sm"></div>
        <div class="col-sm">
          <form>
            <p class="plain_text">Username</p>
            <div class="form-group">
              <input
                type="username"
                v-model="username"
                class="form-control"
                id="exampleInputUsername"
                aria-describedby="usernameHelp"
                placeholder="Enter username"
              />
            </div>
            <br>
            <p class="plain_text">Email</p>
            <div class="form-group">
              <input
                type="email"
                v-model="email"
                class="form-control"
                id="exampleInputEmail1"
                aria-describedby="emailHelp"
                placeholder="Enter email"
              />
            </div>
            <br>
            <p class="plain_text">Password</p>
            <div class="form-group">
              <input
                type="password"
                v-model="password"
                class="form-control"
                id="exampleInputPassword1"
                placeholder="Password"
              />
            </div>
            <br>
            <p class="plain_text">Confirm Password</p>
            <div class="form-group">
              <input
                type="password"
                v-model="passwordConfirmation"
                class="form-control"
                id="exampleInputPassword2"
                placeholder="Confirm Password"
              />
            </div>
            <button type="button" @click="signup" class="btn btn-primary">Submit</button>
          </form>
        </div>
        <div class="col-sm"></div>
      </div>
    </div>
  </div>
</template>


<script>

export default {
  name: 'Registration',
  data() {
    return {
      username: '',
      email: '',
      password: '',
      passwordConfirmation: '',
    }
  },
  methods: {
    signup() {
      if(this.password == this.passwordConfirmation) {
        // initializeApp
        // .auth()
        // .createUserWithEmailAndPassword(this.username, this.password)
        // .then(function() {
        //   console.log("Registration successful");
        // })
        // .catch(function(error) {
        //   console.error("Doslo je do greske", error)
        // })
      }
      else altert("Passwords do not match");
    }
  }
}
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