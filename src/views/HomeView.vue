<template>
  <div class="home">
    <br />
    <br />
    <h1 class="title_text">Welcome to PokéGuesserProject v3</h1>
    <br />
    <p class="plain_text">Please choose your user experience.</p>
    <br />
    <div id="app">
      <!-- <div v-for="p in pokemoni" :key="p">
        {{ p.name }}
        {{ p.primary_type }}
        {{ p.secondary_type }}
        {{ p.primary_colour }}
        {{ p.secondary_colour }}
        {{ p.stage }}
        {{ p.evolution_method }}
      </div> -->
    </div>
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
// @ is an alias to /src

// export default {
//   name: "HomeView",
//   async mounted() {
//     let resp = await fetch("http://localhost:3000/pokemoni");
//     this.pokemoni = await resp.json();
//   },
//   data() {
//     return {
//      pokemoni: [],
//     };
//   },
// };
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
  letter-spacing: 3px;
}
</style>
