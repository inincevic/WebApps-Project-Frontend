<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="normal_text">Primary type*</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputPrimaryType" class="plain_text"></label>
            <input
              type="primaryType"
              class="form-control"
              id="inputPrimaryType"
              aria-describedby="emailHelp"
              placeholder="Enter primary type"
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
        <p class="normal_text">Form</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputForm" class="plain_text"></label>
            <input
              type="form"
              class="form-control"
              id="inputForm"
              aria-describedby="emailHelp"
              placeholder="Enter form"
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
        <p class="normal_text">Dex Entry</p>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <form>
          <div class="form-group">
            <label for="inputDexEntry" class="plain_text"></label>
            <input
              type="dexEntry"
              class="form-control"
              id="inputDexEntry"
              aria-describedby="emailHelp"
              placeholder="Enter dex entry"
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">
          Type a piece of or entire dex entry of this Pokémon. <br />
          (Note: might not be implemented)
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
            />
          </div>
        </form>
      </div>
      <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4">
        <p class="explanation">Enter this Pokémon's base stat total.</p>
      </div>
    </div>

    <button
      type="submit"
      class="btn btn-success btn-lg"
      style="
        margin: 1em;
        font-family: 'Pokemon Solid';
        color: #2a75bb;
        background-color: #ffcb05;
      "
    >
      <router-link to="/foundguest">Continue</router-link>
      <!-- Note: will have to create this page with display once database and backend communication are complete -->
    </button>
  </div>
</template>

<script></script>

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
