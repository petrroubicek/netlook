<template>
  <div class="popup">
    <div class="popup__content">
      <button
        type="button"
        class="popup__content-close btn btn--icon btn--close"
        @click="showHomeFN()"
      >X</button>
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
@import "../assets/scss/_mixins.scss";

.popup {
  position: fixed;
  display: flex;
  left: 0px;
  top: 0px;
  height: 100%;
  width: 100%;

  &__content {
    position: absolute;
    top: 50%;
    left: calc(50% - 2px);
    transform: translate(-50%, -50%);
    margin: 0px;
    padding: 20px;
    height: auto;
    width: calc(100% - 80px);
    background: #eee;
    z-index: 10;
    @include border-radius(20px);

    &-header {
      margin: 0px auto;
      height: 48px;
      width: 48px;
      @include border-radius(100%);
      background: url("../../assets/img/profil.png");

      img {
        height: 48px;
        width: 48px;
        @include border-radius(100%);
      }
    }

    &-close {
      position: absolute;
      left: 0px;
      top: 0px;
      padding: 0px;
      color: #aaa;
    }
  }

  &__overlay {
    @include overlay(#333, 1);
  }
}
</style>


