<template>
  <div class="container">
    <div class="welcome">
      <div class="title">WELCOME TO <span>EDUCATION</span></div>
      <div class="text">
        Vivamus sed porttitor felis. Pellentesque habitant morbi tristique
        senectus et netus et malesuada fames ac turpis egestas.Sed lorem enim,
        Vivamus sed porttitor felis. Pellentesque habitant morbi tristique
        senectus et netus et malesuada fames ac turpis egestas.Sed lorem enim,
      </div>
    </div>
    <div class="whatwedo">
      <div class="title">WHAT <span>WE DO</span></div>
      <div class="cards">
        <Card v-for="item in cardsText" :key="item.title" :detail="item" />
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card";

export default {
  data() {
    return {
      cardsText: [
        {
          image: require("../../imgs/hat.svg"),
          image_blue: require("../../imgs/hat_blue.svg"),
          title: "PROFESSIONAL STUDY",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing.",
        },
        {
          image: require("../../imgs/book.svg"),
          image_blue: require("../../imgs/book_blue.svg"),
          title: "SUMMER SESSION",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing.",
        },
        {
          image: require("../../imgs/earth.svg"),
          image_blue: require("../../imgs/earth_blue.svg"),
          title: "GLOBAL EDUCATION",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing.",
        },
      ],
    };
  },
  components: {
    Card,
  },
};
</script>

<style lang="less" scoped>
.container {
  width: 1100px;
  margin-left: 50%;
  transform: translateX(-50%);
  padding: 50px 0 100px 0;
  .title {
    letter-spacing: 2px;
    font-size: 40px;
    color: #000;
    font-family: "Montserrat-SemiBold", sans-serif;
    span {
      color: #cc2105;
    }
  }
  .welcome {
    .text {
      margin-top: 50px;
      width: 500px;
      color: #333;
      font-size: 15px;
      line-height: 1.8;
      letter-spacing: 1px;
    }
  }
  .whatwedo {
    margin-top: 200px;
    text-align: center;
    .cards {
      margin-top: 50px;
      display: flex;
      justify-content: space-between;
    }
  }
}
</style>