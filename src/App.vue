<template>
  <div id="app">
    <div class="container">
      <h1 class="title">VÍTEJTE</h1>
      <p class="description">Výsledné řešení se nachází
        <br>po kliknutí na konkrétní button.
      </p>

      <!--% ÚLOHY -->
      <button type="button" class="start-button btn btn--primary btn--radius">Show popup #1</button>
      <button type="button" class="start-button btn btn--primary btn--radius">Show popup #2</button>
      <button type="button" class="start-button btn btn--primary btn--radius">Show content</button>

      <!--% KONTAKT -->
      <a
        href="tel:777556047"
        class="contact-button btn btn--primary btn--radius btn--border"
      >Zavolat řešiteli</a>

      <PopUp/>
      <Content/>
    </div>
  </div>
</template>

<script>
import PopUp from "./components/PopUp";
import Content from "./components/Content";

export default {
  name: "App",
  components: {
    PopUp,
    Content
  },
  methods: {
    showPopUp() {}
  }
};
</script>

<style lang="scss">
@import "./assets/scss/_variables.scss";
@import "./assets/scss/_mixins.scss";
@import "./assets/scss/_buttons.scss";

body {
  margin: 0px;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

.container {
  position: relative;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  margin: 0px auto;
  height: $default-device-height;
  width: $default-device-width;
}

.title {
  margin: 10% 0px 30px;
  color: $main-color;
  text-transform: uppercase;
}
.description {
  margin: 0px 0px 30px;
  line-height: 1.5;
  color: $minor-color;
}

.start-button {
  margin: 20px 40px;
}
.contact-button {
  margin: 50px 40px 10px;
}
</style>
