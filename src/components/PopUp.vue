<template>
  <div>
    <h2 class="test">popup</h2>

    <div class="popup">
      <button type="button">X</button>
      <div class="popup__header">
        <img src>
      </div>
      <div class="popup__body">
        <h2>Test</h2>
        <p>Some text ...</p>
      </div>
      <div class="popup__footer">
        <button type="button">BTN1</button>
        <button type="button">BTN0</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PopUp"
};
</script>

<style lang="scss" scoped>
.popup {
  background: #eee;
  //@include border-radius(20px);
}
</style>


