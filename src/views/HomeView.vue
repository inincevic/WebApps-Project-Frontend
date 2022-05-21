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
      Log in
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
      Guest
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
      Register
    </button>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
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
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 35px;
}
</style>
