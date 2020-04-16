<template>
  <div class="popup">
    <div class="popup__content">
      <button
        type="button"
        class="popup__content-close btn btn--icon btn--close"
        @click="showHomeFN()"
      ></button>
      <div class="popup__content-header">
        <img v-if="profileImg" :src="profileImg" class="popup__content-header">
      </div>
      <div class="popup__content-body">
        <h2>{{title}}</h2>
        <p>{{message}}</p>
      </div>
      <div class="popup__content-footer">
        <button type="button" class="btn btn--primary btn--radius">{{btn1}}</button>
        <button type="button" class="btn">{{btn2}}</button>
      </div>
    </div>
    <div class="popup__overlay"></div>
  </div>
</template>

<script>
export default {
  name: "PopUp",
  props: {
    selectedComponent: String,
    profileImg: String,
    title: String,
    message: String,
    btn1: String,
    btn2: String,
    showHomeFN: Function
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_popup.scss";
</style>


