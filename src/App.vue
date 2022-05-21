<template>
  <div id="app">
    <nav id="nav" class="navbar navbar-light bg-light">
      <p class="navbar_title">PokéGuesserProject</p>
      <router-link to="/" class="navbar_element">Home</router-link>
      <router-link to="/about" class="navbar_element">About</router-link>
    </nav>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.navbar_title {
  text-align: center;
  font-family: "Pokemon Solid";
  color: #ffcb05;
  font-size: 30px;
}

.navbar_element {
  font-family: "Pokemon Hollow";
  color: #ffcb05;
  font-size: 30px;
  margin: 10px;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
