<template>
  <div class="popup">
    <div class="popup-content">
      <button
        type="button"
        class="popup-content__close btn btn--icon btn--close"
        @click="showHomeFN()"
      ></button>
      <div
        class="popup-content__header"
        v-bind:class="{'popup-content__header--badge': profileImg}"
      >
        <img v-if="profileImg" :src="profileImg">
      </div>
      <div class="popup-content__body">
        <h2 v-bind:class="{'double-row': doubleRowTitle}">{{title}}</h2>
        <p>{{message}}</p>
      </div>
      <div
        class="popup-content__footer"
        v-bind:class="{'popup-content__footer--vertical': !btnHorizontal}"
      >
        <button type="button" :class="btn1Class">{{btn1Text}}</button>
        <button type="button" :class="btn2Class">{{btn2Text}}</button>
      </div>
    </div>
    <div class="popup-overlay"></div>
  </div>
</template>

<script>
export default {
  name: "PopUp",
  props: {
    selectedComponent: String,
    profileImg: String,
    title: String,
    doubleRowTitle: Boolean,
    message: String,
    btnHorizontal: Boolean,
    btn1Text: String,
    btn1Class: String,
    btn2Text: String,
    btn2Class: String,
    showHomeFN: Function
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_popup.scss";
</style>


