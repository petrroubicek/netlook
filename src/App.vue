<template>
  <div id="app">
    <div class="container">
      <!-- HOMEPAGE -->
      <Home
        v-if="part == 'Home'"
        :selectedComponent="part"
        :showPopUpFN="showPopUp"
        :showContentFN="showContent"
      ></Home>
      <!-- POPUP -->
      <PopUp
        v-if="part == 'PopUp'"
        :selectedComponent="part"
        :profileImg="popUp.profileImg"
        :title="popUp.title"
        :doubleRowTitle="popUp.doubleRowTitle"
        :message="popUp.message"
        :btnHorizontal="popUp.btnHorizontal"
        :btn1Text="popUp.btn1Text"
        :btn1Class="popUp.btn1Class"
        :btn2Text="popUp.btn2Text"
        :btn2Class="popUp.btn2Class"
        :showHomeFN="showHome"
      ></PopUp>
      <!-- CONTENT -->
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
        title: "",
        doubleRowTitle: false,
        description: "",
        btnHorizontal: false,
        btn1Text: "",
        btn1Class: "",
        btn2Text: "",
        btn2Class: ""
      }
    };
  },
  methods: {
    showPopUp(
      profileImg,
      title,
      doubleRowTitle,
      message,
      btnHorizontal,
      btn1Text,
      btn1Class,
      btn2Text,
      btn2Class
    ) {
      this.part = "PopUp";
      this.popUp.profileImg = profileImg;
      this.popUp.title = title;
      this.popUp.doubleRowTitle = doubleRowTitle;
      this.popUp.message = message;
      this.popUp.btnHorizontal = btnHorizontal;
      this.popUp.btn1Text = btn1Text;
      this.popUp.btn1Class = btn1Class;
      this.popUp.btn2Text = btn2Text;
      this.popUp.btn2Class = btn2Class;
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
@import "/public/_fonts.scss";
@import "./assets/scss/_variables.scss";
@import "./assets/scss/_mixins.scss";
@import "./assets/scss/_buttons.scss";
@import "./assets/scss/_layout.scss";
</style>
