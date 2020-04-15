<template>
  <div id="app">
    <div class="container">
      <button type="button" class="btn btn--primary">Show popup #1</button>
      <button type="button" class="btn btn--primary">Show popup #2</button>
      <button type="button" class="btn btn--primary">Show content</button>
      
      <PopUp  />
      <Content />
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
    showPopUp() {

    }
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
  flex-wrap: wrap;
  margin: 0px auto;
  height: $default-device-height;
  width: $default-device-width;
}
</style>
