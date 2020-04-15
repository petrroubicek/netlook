<template>
  <div class="row">
    <h1 class="title">VÍTEJTE</h1>
    <p class="description">Výsledné řešení se nachází
      <br>po kliknutí na konkrétní button.
    </p>
    <!--% ÚLOHY -->
    <button
      type="button"
      class="component-button btn btn--primary btn--radius"
      @click="showPopUpFN(datas.popUp1.profileImg, datas.popUp1.title, datas.popUp1.message, datas.popUp1.btn1, datas.popUp1.btn2)"
    >Show popup #1</button>
    <button
      type="button"
      class="component-button btn btn--primary btn--radius"
      @click="showPopUpFN(datas.popUp2.profileImg, datas.popUp2.title, datas.popUp2.message, datas.popUp2.btn1, datas.popUp2.btn2)"
    >Show popup #2</button>
    <button
      type="button"
      class="component-button btn btn--primary btn--radius"
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
    showPopUpFN: Function,
    showContentFN: Function
  },
  data() {
    return {
      datas: {
        popUp1: {
          profileImg: "",
          title: "Title example for two rows",
          message: "Random text all users will see. You",
          btn1: "Btn1",
          btn2: "Btn3"
        },
        popUp2: {
          profileImg:
            "https://i.pinimg.com/originals/21/36/91/21369158540994fa57bf2f250f88a2dd.jpg",
          title: "Title example for two rows",
          message: "Random text all users will see. You don´t know",
          btn1: "Btn2",
          btn2: "Btn1"
        }
      }
    };
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

.component-button {
  margin: 20px 40px;
  height: 50px;
}
.contact-button {
  margin: 60px 40px 10px;
}
</style>