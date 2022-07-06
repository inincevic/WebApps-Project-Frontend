<template>
  <div class="home">
    <br />
    <br />
    <h1 class="title_text">Welcome to PokéGuesserProject v3</h1>
    <br />
    <p class="plain_text">Please choose your user experience.</p>
    <br />
    <button
      type="button"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
    >
      <router-link to="/login">Login</router-link>
    </button>
    <button
      type="button"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
    >
      <router-link to="/guest">Guest</router-link>
    </button>
    <button
      type="button"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
    >
      <router-link to="/registration">Register</router-link>
    </button>
  </div>
</template>

<script>

export default {
  name: "HomeView",
  created() {
    localStorage.clear();
  }
};
</script>

<style scoped>
@import url(//db.onlinewebfonts.com/c/9b6de539b8ae4ce6ef9b137bb7764413?family=Pokemon++Solid); /* font-family: 'Pokemon Solid', sans-serif; */
@import url(//db.onlinewebfonts.com/c/77b688bb2949f59670224cb24e8e8144?family=Pokemon++Hollow); /* font-family: 'Pokemon Hollow', sans-serif; */
@import url(//db.onlinewebfonts.com/c/6120639772c6c60a2fad6742051c6feb?family=Unown);

.title_text {
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 75px;
}

.plain_text {
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 35px;
  letter-spacing: 3px;
}
</style>
