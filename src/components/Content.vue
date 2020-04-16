<template>
  <div class="content">
    <!-- TITLE -->
    <h2 class="content-title">N steps to earn revenue</h2>

    <!-- STEP -->
    <div class="content-step" v-for="(item, x) in steps" :key="x">
      <img :src="item.stepImg" class="content-step__img">
      <div class="content-step__box">
        <h2>{{item.stepTitle}}</h2>
        <a v-if="item.link" href="#">{{item.stepDescription}}</a>
        <span v-if="!item.link">{{item.stepDescription}}</span>
      </div>
    </div>

    <!-- BACK HOME -->
    <button
      type="button"
      class="content-back btn btn--primary btn--radius"
      @click="showHomeFN()"
    >Back home</button>
  </div>
</template>

<script>
export default {
  name: "Content",
  props: {
    showHomeFN: Function
  },
  data() {
    return {
      steps: [
        {
          stepImg: "../images/step1.png",
          stepTitle: "Create account",
          stepDescription:
            "Signing up is easy, it will take just a minute and then you are ready to receive gifts",
          stepLink: true
        },
        {
          stepImg: "../images/step2.png",
          stepTitle: "Share your life",
          stepDescription:
            "Set prices and start chat with people, post pictures & videos, make calls. Everything you",
          stepLink: false
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_content.scss";
</style>


