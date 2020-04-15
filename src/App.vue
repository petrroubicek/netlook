<template>
  <div id="app">
    <div class="container">
      <Home
        v-if="part == 'Home'"
        :selectedComponent="part"
        :showPopUpFN="showPopUp"
        :showContentFN="showContent"
      ></Home>
      <PopUp
        v-if="part == 'PopUp'"
        :selectedComponent="part"
        :profileImg="popUp.profileImg"
        :title="popUp.title"
        :message="popUp.message"
        :btn1="popUp.btn1"
        :btn2="popUp.btn2"
        :showHomeFN="showHome"
      ></PopUp>
      <Content v-if="part == 'Content'" :selectedComponent="part" :showHomeFN="showHome"></Content>
    </div>
  </div>
</template>

<script>
import Home from "./components/Home";
import PopUp from "./components/PopUp";
import Content from "./components/Content";

export default {
  name: "App",
  data() {
    return {
      part: "Home",
      popUp: {
        profileImg: "",
        title: "test",
        description: "Random text all users will see. You",
        btn1: "Btn1",
        btn2: "Btn3"
      },
    };
  },
  methods: {
    showPopUp(profileImg, title, message, btn1, btn2) {
      this.part = "PopUp";
      this.popUp.profileImg = profileImg;
      this.popUp.title = title;
      this.popUp.message = message;
      this.popUp.btn1 = btn1;
      this.popUp.btn2 = btn2;
      //this.$emit("changePart", this.selectedComponent);
    },
    showContent() {
      this.part = "Content";
    },
    showHome() {
      this.part = "Home";
    }
  },
  components: {
    Home,
    PopUp,
    Content
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
  justify-content: center;
  margin: 0px auto;
  height: $default-device-height;
  width: $default-device-width;
}
</style>
