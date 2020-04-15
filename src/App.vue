<template>
  <div id="app">
    <div class="container">
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
  }
};
</script>

<style lang="scss">
@import "./assets/scss/_variables.scss";

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
  margin: 0px auto;
  height: $default-device-height;
  width: $default-device-width;
}
</style>
