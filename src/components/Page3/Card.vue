<template>
  <div class="card">
    <img :src="image" />
    <div class="title">EDUCATION</div>
    <div class="text">Lorem ipsum dolor sit amet consectetur adipisicing.</div>
  </div>
</template>

<script>
export default {
  props: {
    imageName: String,
  },
  computed: {
    image() {
      switch (this.imageName) {
        case "earth":
          return require("../../imgs/earth.svg");
        case "hat":
          return require("../../imgs/hat.svg");
        case "book":
          return require("../../imgs/book.svg");
        default:
          return require("../../imgs/earth.svg");
      }
    },
  },
};
</script>

<style lang="less" scoped>
.card {
  background: #ffffff;
  height: 250px;
  width: 270px;
  padding: 25px 40px 25px 25px;
  margin-top: 40px;
  img {
    width: 40px;
  }
  .title {
    font-family: "Montserrat-SemiBold", sans-serif;
    font-size: 18px;
    letter-spacing: 2px;
    font-weight: 600;
    margin-top: 10px;
  }
  .text {
    margin-top: 20px;
    color: #333;
    font-size: 15px;
    line-height: 1.8;
    letter-spacing: 1px;
    width: 80%;
  }
}
</style>