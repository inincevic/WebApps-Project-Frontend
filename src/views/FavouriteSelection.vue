<template>
  <div class="about">
    <br />
    <br />
    <h1 class="title_text">
      {{ userInfo.username }}, please write the name of your favourite Pokémon
    </h1>
    <br />
    <br />
    <br />
    <p class="plain_text">
      Current favourite Pokémon: {{ userInfo.favourite_pokemon }}
    </p>
    <p class="plain_text">
      Favourite Pokémon: {{ userInfo.favourite_pokemon }}
    </p>
    <br />
    <div class="form-group">
      <div class="col-xs-5" style="margin-left: 15px">
        <input
          type="email"
          class="form-control"
          id="exampleInputPokemon"
          placeholder="New favourite Pokémon"
          v-model="userInfo.new_favourtie_pokemon"
        />
      </div>
      <div class="col-xs-5"></div>
    </div>
    <br />
    <br />
    <br />
    <br />
    <div>
      <div class="col-xs-4"></div>
      <div class="col-xs-4" align="center">
        <div class="sub_text">Save your selection</div>
        <button
        type="button"
        class="btn btn-success btn-lg"
        style="
          margin-left: 1000 px;
          margin-top: 20px;
          font-family: 'Pokemon Solid';
          color: #2a75bb;
          background-color: #ffcb05;
        "
      >
        Save
      </button>
      </div>
      <div class="col-xs-4">
        <div class="sub_text">Return to profile</div>
      </div>
    </div>
    <br />
    <div class="col-xs-4"></div>
    <div class="col-xs-4">
      
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
      <router-link to="/profile">Return</router-link>
    </button>
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
        favourite_pokemon: "",
        new_favourtie_pokemon: "",
      },
    };
  },
  created() {
    this.userInfo.username = localStorage.getItem("username");
    this.userInfo.favourite_pokemon = localStorage.getItem("favourite_pokemon");
    if (this.userInfo.favourite_pokemon == "") {
      this.userInfo.favourite_pokemon = "Not set.";
    }
  },
  methods: {
    async updateFavourite() {
            
    }
  }
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
  margin-left: 30px;
  letter-spacing: 3px;
}

</style>
