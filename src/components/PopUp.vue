<template>
  <div class="popup">
    <div class="popup__content">
      <button type="button">X</button>
      <div class="popup__content-header">
        <img src>
      </div>
      <div class="popup__content-body">
        <h2>Test</h2>
        <p>Some text ....</p>
      </div>
      <div class="popup__content-footer">
        <button type="button" class="btn btn--primary">BTN1</button>
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
  height: 100%;
  width: 100%;

  &__content {
    position: absolute;
    top: 50%;
    left: calc(50% - 15px);
    transform: translate(-50%, -50%);
    margin: 0px;
    padding: 20px;
    height: auto;
    width: calc(100% - 100px);
    background: #eee;
    z-index: 10;
    @include border-radius(20px);
  }

  &__overlay {
    @include overlay(#333, 1);
  }
}
</style>


