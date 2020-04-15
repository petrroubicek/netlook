<template>
  <div class="popup">
    <div class="popup__content">
      <button type="button" class="popup__content-close btn btn--icon btn--close">X</button>
      <div class="popup__content-header">
        <img
          src="https://i.pinimg.com/originals/21/36/91/21369158540994fa57bf2f250f88a2dd.jpg"
          class="popup__content-header"
        >
      </div>
      <div class="popup__content-body">
        <h2>Test</h2>
        <p>Some text ....</p>
      </div>
      <div class="popup__content-footer">
        <button type="button" class="btn btn--primary btn--radius">BTN1</button>
        <button type="button" class="btn">BTN0</button>
      </div>
    </div>
    <div class="popup__overlay"></div>
  </div>
</template>

<script>
export default {
  name: "PopUp"
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
  //display: none;

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


