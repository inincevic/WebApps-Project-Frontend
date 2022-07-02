<template>
  <div class="about">
    <br />
    <br />
    <h1 class="title_text">Welcome {{ userInfo.username }}</h1>
    <br />
    <br>
    <p class="plain_text">
      Number of guessed Pokémon: {{userInfo.number_guessed}}
    </p>
    <p class="plain_text">
      Favourite Pokémon: {{userInfo.favourite_pokemon}}
    </p>
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
  created() {
    this.userInfo.username = localStorage.getItem("username");
    this.userInfo.number_guessed = localStorage.getItem("number_guessed");
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
</style>
