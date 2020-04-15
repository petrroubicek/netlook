<template>
  <div id="app">
    <PopUp/>
    <Content/>
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
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

// MIXINS
@mixin border-radius($pixel...) {
  border-radius: $pixel;
  -webkit-border-radius: $pixel;
  -moz-border-radius: $pixel;
}

// VARIABLES
$main-color: purple;
$minor-color: #eee;
</style>
