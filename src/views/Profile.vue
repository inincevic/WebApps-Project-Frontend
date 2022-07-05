<template>
  <div class="about">
    <br />
    <br />
    <h1 class="title_text">Welcome {{ userInfo.username }}</h1>
    <br />
    <br />
    <p class="plain_text">
      Number of guessed Pokémon: {{ userInfo.number_guessed }}
    </p>
    <p class="plain_text">
      Favourite Pokémon: {{ userInfo.favourite_pokemon }}
    </p>
    <p class="sub_text">
      Set favourite Pokémon.
    </p>
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
      <router-link to="/FavouriteSelection">Select</router-link>
    </button>
  </div>

  <div>
    <div class="col-xs-4">
    <p class="sub_text">List of all the Pokémon you guessed</p>
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
      <router-link to="/GuessedList">List</router-link>
    </button>
    </div>
    <div class="col-xs-4">
    <p class="sub_text">Pokémon guessing</p>
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
      <router-link to="">Select</router-link>
    </button>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Profile",
  data() {
    return {
      userInfo: {
        username: "",
        number_guessed: "",
        favourite_pokemon: "",
      },
    };
  },
  methods:{
    async replace_name(){
      if(localStorage.getItem("favourite_pokemon") != ""){
        await axios
        .post("http://localhost:3000/favouritename", this.userInfo)
        .then(async (response) => {
          localStorage.removeItem("favourite_pokemon");
          localStorage.setItem("favourite_pokemon", response.data);
        });
      }
      else{
        this.userInfo.favourite_pokemon = "Not set.";
      }
    }
  },
  async created() {
    this.userInfo.username = localStorage.getItem("username");
    this.userInfo.number_guessed = localStorage.getItem("number_guessed");
    this.userInfo.favourite_pokemon = localStorage.getItem("favourite_pokemon");
    await this.replace_name();
    this.userInfo.favourite_pokemon = localStorage.getItem("favourite_pokemon");
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
  text-align: left;
  margin-left: 30px;
  letter-spacing: 4px;
}

.plain_text {
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 35px;
  text-align: left;
  margin-left: 30px;
  letter-spacing: 3px;
}
.sub_text {
  color: #ffcb05;
  font-family: "Pokemon Solid", sans-serif;
  font-size: 25px;
  text-align: left;
  margin-left: 400px;
  margin-top: 50px;
  letter-spacing: 3px;
}
</style>
