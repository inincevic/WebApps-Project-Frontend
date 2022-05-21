<template>
  <div class="home">
    <h1 class="title_text">Welcome to PokeGuesserProject v3</h1>
    <br />
    <p class="plain_text">Please choose your user experience.</p>
    <br />
    <div class="btn-space">
      <button type="button" class="btn btn-primary">Log in</button>
      <button type="button" class="btn btn-success">Guest</button>
      <button type="button" class="btn btn-info">Register</button>
    </div>
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

.title_text {
  color: black;
  font-family: "Pokemon Hollow", sans-serif;
  font-size: 75px;
}

.plain_text {
  color: black;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 30px;
}

.btn-space {
    margin-right: 5px;
}
</style>
