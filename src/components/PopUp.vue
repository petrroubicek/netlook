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
  display: flex;
  

  &__content {
    padding: 20px;
    width: 100%;
    background: #eee;
    z-index: 10;
    @include border-radius(20px);
  }

  &__overlay {
    @include overlay;
  }
}
</style>


