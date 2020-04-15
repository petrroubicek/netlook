<template>
  <div class="row">
    <h1 class="title">VÍTEJTE</h1>
    <p class="description">Výsledné řešení se nachází
      <br>po kliknutí na konkrétní button.
    </p>
    <!--% ÚLOHY -->
    <button
      type="button"
      class="start-button btn btn--primary btn--radius"
      @click="showPopUpFN()"
    >Show popup #1</button>
    <button
      type="button"
      class="start-button btn btn--primary btn--radius"
      @click="showPopUpFN()"
    >Show popup #2</button>
    <button
      type="button"
      class="start-button btn btn--primary btn--radius"
      @click="showContentFN()"
    >Show content</button>

    <!--% KONTAKT -->
    <a
      href="tel:777556047"
      class="contact-button btn btn--primary btn--radius btn--border"
    >Zavolat řešiteli</a>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    selectedComponent: String,
    popUpData: Array,
    showPopUpFN: Function,
    showContentFN: Function
  }
};
</script>

<style lang="scss">
@import "../assets/scss/_variables.scss";
@import "../assets/scss/_mixins.scss";

.row {
  display: flex;
  flex-flow: column;
}

.title {
  margin: 0px 0px 30px;
  color: $main-color;
  text-transform: uppercase;
}
.description {
  margin: 0px 0px 40px;
  line-height: 1.5;
  color: $minor-color;
}

.start-button {
  margin: 20px 40px;
  height: 50px;
}
.contact-button {
  margin: 60px 40px 10px;
}
</style>