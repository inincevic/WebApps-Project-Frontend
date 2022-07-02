<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Primary type*</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form
          @submit="sendPokemonCredentials()"
          action="#"
          onsubmit="return false"
        >
          <div class="form-group">
            <label for="inputPrimaryType" class="plain_text"></label>
            <input
              type="primaryType"
              class="form-control"
              id="inputPrimaryType"
              aria-describedby="emailHelp"
              placeholder="Enter primary type"
              v-model="enteredAtributes.type_one"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what the primary type of the Pokémon is. <br />
          Note: Add the list of possible types
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Secondary type</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputSecondaryType" class="plain_text"></label>
            <input
              type="secondaryType"
              class="form-control"
              id="inputSecondaryType"
              aria-describedby="emailHelp"
              placeholder="Enter secondary type"
              v-model="enteredAtributes.type_two"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what the secondary type of the Pokémon is. <br />
          Note: Add the list of possible types
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Primary colour*</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputPrimaryColour" class="plain_text"></label>
            <input
              type="primaryColour"
              class="form-control"
              id="inputPrimaryColour"
              aria-describedby="emailHelp"
              placeholder="Enter primary colour"
              v-model="enteredAtributes.colour_one"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what the dominant of the Pokémon is. <br />
          Note: Add the list of possible colours
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Secondary colour</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputSecondaryColour" class="plain_text"></label>
            <input
              type="secondaryColour"
              class="form-control"
              id="inputSecondaryColour"
              aria-describedby="emailHelp"
              placeholder="Enter secondary colour"
              v-model="enteredAtributes.colour_two"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what the second dominant colour of the Pokémon is. <br />
          Note: Add the list of possible colours
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Stage</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputForm" class="plain_text"></label>
            <input
              type="stage"
              class="form-control"
              id="inputForm"
              aria-describedby="emailHelp"
              placeholder="Enter form"
              v-model="enteredAtributes.stage"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what is the form of this Pokémon. <br />
          (Base form, 1st stage, 2nd stage)
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Evolution method</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputEvolutionMethod" class="plain_text"></label>
            <input
              type="evolutionMethod"
              class="form-control"
              id="inputEvolutionMethod"
              aria-describedby="emailHelp"
              placeholder="Enter evolution method"
              v-model="enteredAtributes.evolution_method"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what method is needed for this Pokémon to reach this stage from
          it's previous stage. <br />Note: Add the list of possible methods
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Regional variant</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputRegionalVariant" class="plain_text"></label>
            <input
              type="regionalVariant"
              class="form-control"
              id="inputRegionalVariant"
              aria-describedby="emailHelp"
              placeholder="Enter regional variant"
              v-model="enteredAtributes.regional_variant"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type what regional variant this Pokémon is. <br />
          (Original, Alolan, Galarian, Hisuian)
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Base stat total</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputBaseStatTotal" class="plain_text"></label>
            <input
              type="baseStatTotal"
              class="form-control"
              id="inputBaseStatTotal"
              aria-describedby="emailHelp"
              placeholder="Enter base stat total"
              v-model="enteredAtributes.base_stat_total"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">Enter this Pokémon's base stat total.</p>
      </div>
    </div>

    <!-- Displaying data entered into fields. Use only to check if the fields work -->
    <!-- <div>
      {{enteredAtributes.type_one}}
      <br>
      {{enteredAtributes.type_two}}
      <br>
      {{enteredAtributes.colour_one}}
      <br>
      {{enteredAtributes.colour_two}}
      <br>
      {{enteredAtributes.form}}
      <br>
      {{enteredAtributes.evolution_method}}
      <br>
      {{enteredAtributes.regional_variant}}
      <br>
      {{enteredAtributes.base_stat_total}}
    </div> -->
    <button
      type="submit"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
      @click="sendPokemonCredentials()"
    >
      <router-link to="/foundguest">Continue</router-link>
      <!-- Note: will have to create this page with display once database and backend communication are complete -->
    </button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "GuestGuess",

  methods: {
    async setPokemon(response) {
      localStorage.setItem("foundPokemonNumber", response.data.dex_number);
      localStorage.setItem("foundPokemonName", response.data.pokemon_name);
      localStorage.setItem(
        "foundPokemonTypeOne",
        response.data.types[0].type_id
      );
      if (response.data.types.length > 1) {
        localStorage.setItem(
          "foundPokemonTypeTwo",
          response.data.types[1].type_id
        );
      }
      localStorage.setItem(
        "foundPokemonColourOne",
        response.data.colours[0].colour_id
      );
      if (response.data.colours.length > 1) {
        localStorage.setItem(
          "foundPokemonColourTwo",
          response.data.colours[1].colour_id
        );
      }
      localStorage.setItem("foundPokemonStage", response.data.stage);
      localStorage.setItem(
        "foundPokemonEvolutionMethod",
        response.data.evolution_method
      );
      localStorage.setItem("foundPokemonRegionalVariant", response.data.form);
      localStorage.setItem("foundPokemonBST", response.data.base_stat_total);
      localStorage.setItem("foundPokemonEntry", response.data.dex_entry);
    },

    removeFromStorage() {
      localStorage.removeItem("foundPokemonNumber");
      localStorage.removeItem("foundPokemonName");
      localStorage.removeItem("foundPokemonTypeOne");
      localStorage.removeItem("foundPokemonTypeTwo");
      localStorage.removeItem("foundPokemonColourOne");
      localStorage.removeItem("foundPokemonColourTwo");
      localStorage.removeItem("foundPokemonStage");
      localStorage.removeItem("foundPokemonEvolutionMethod");
      localStorage.removeItem("foundPokemonRegionalVariant");
      localStorage.removeItem("foundPokemonBST");
      localStorage.removeItem("foundPokemonEntry");
    },

    sendPokemonCredentials() {
      axios
        .post("http://localhost:3000/findpokemon", this.enteredAtributes)
        .then((response) => {
          console.log("recieved response");
          console.log(response);
          if (response.data) {
            this.removeFromStorage();
            this.setPokemon(response);
            this.$router.push({
              name: "foundguest",
            });
          }
          //push to 404 pokemon not found
        });
    },
  },

  data() {
    return {
      enteredAtributes: {
        type_one: "",
        type_two: "",
        colour_one: "",
        colour_two: "",
        stage: "",
        evolution_method: "",
        regional_variant: "",
        base_stat_total: "",
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
  letter-spacing: 3px;
}

.plain_text {
  color: black;
  font-family: "Unown", sans-serif;
  font-size: 35px;
}

.normal_text {
  color: #ffcb05;
  font-family: "Times New Roman", Times, serif;
  font-size: 30px;
}

.explanation {
  color: #ffcb05;
  font-family: "Times New Roman", Times, serif;
  font-size: 20px;
}
</style>
