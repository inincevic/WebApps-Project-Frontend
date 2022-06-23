<template>
  <div class="about">
    <h1 class="title_text">The Pokémon is</h1>
    <br>
    <div class="display_div">
        <p class="normal_text"> 
            Name:  {{pokemon.name}}
            <br>
            Type: {{pokemon.types.type_one}}, {{pokemon.types.type_two}}
            <br>
            Colours: {{pokemon.colours.colour_one}}, {{pokemon.colours.colour_two}}
            <br>
            Form: {{pokemon.form}}
            <br>
            Evolution {{pokemon.evolution_method}}
            <br>
            Regional variant: {{pokemon.regional_variant}}
            <br>
            Dex entry: {{pokemon.dex_entry}}
            <br>
            Base stat total: {{pokemon.base_state_total}}
        </p>
    </div>

    <button
      type="button"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-size: 25px;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
    >
      <router-link to="/">Home</router-link>
      <!-- Note: will have to create this page with display once database and backend communication are complete -->
    </button>

  </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            pokemon: {
                name: "test",
                types: {
                    type_one: "test",
                    type_two: "test"},
                colours: {
                    colour_one: "test",
                    colour_two: "test"},
                form: "test",
                evolution_method: "test",
                regional_variant: "test",
                dex_entry: "test",
                base_state_total: "test"
            }
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
  color: #ffcb05;
  font-family: "Unown", sans-serif;
  font-size: 50px;
}

.normal_text {
  color: #ffcb05;
  font-family: "Times New Roman", Times, serif;
  text-align: left;
  font-size: 35px;
}

.display_div {
    margin-left: 200px;
}


</style>