<template>
  <div class="container">
    <h3>RECENT <span>FEEDBACK</span></h3>
    <div class="rotationContainer">
      <div class="rotation" :style="rotationStyle">
        <Card v-for="person in cards" :key="person.name" :person="person" />
      </div>
      <div class="switcher">
        <img src="../../imgs/left.png" @click="toLeft" />
        <img src="../../imgs/right.png" @click="toRight" />
      </div>
      <div class="navPoint" ref="navPoint">
        <div
          class="point"
          v-for="(i, index) in pointNum"
          :key="i"
          @click="jumpNav(index)"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Page5",
  components: {
    Card,
  },
  data() {
    return {
      cards: [
        { name: "Mary Jane", image: require("../../imgs/te1.jpg") },
        { name: "Olivia Ruth", image: require("../../imgs/te3.jpg") },
        { name: "Blake Joe", image: require("../../imgs/te2.jpg") },
        { name: "Mary Jane", image: require("../../imgs/te4.jpg") },
        { name: "Olivia Ruth", image: require("../../imgs/te5.jpg") },
        { name: "Blake Joe", image: require("../../imgs/te6.jpg") },
        { name: "Mary Jane", image: require("../../imgs/te1.jpg") },
        { name: "Olivia Ruth", image: require("../../imgs/te3.jpg") },
        { name: "Blake Joe", image: require("../../imgs/te2.jpg") },
      ],
      currentPic: 0,
      rotateTimer: {},
    };
  },
  computed: {
    rotationStyle() {
      return "left: -" + 370 * this.currentPic + "px";
    },
    pointNum() {
      if (this.cards.length % 3 === 0) {
        return this.cards.length / 3;
      }
      return this.cards.length / 3 + 1;
    },
  },
  watch: {
    currentPic(val) {
      this.$refs.navPoint.children.forEach(
        (i) => (i.style.background = "#c1bebe")
      );
      this.$refs.navPoint.children[parseInt(val / 3)].style.background =
        "#ffffff";
    },
  },
  mounted() {
    this.rotate();

    this.$refs.navPoint.children[0].style.background = "#ffffff";
  },
  methods: {
    rotate() {
      this.rotateTimer = setInterval(() => {
        if (this.currentPic < this.cards.length - 3) {
          this.currentPic++;
        } else {
          this.currentPic = 0;
        }
      }, 3000);
    },
    toLeft() {
      clearInterval(this.rotateTimer);
      if (this.currentPic > 0) {
        this.currentPic--;
      }
      this.rotate();
    },
    toRight() {
      clearInterval(this.rotateTimer);
      if (this.currentPic < this.cards.length - 3) {
        this.currentPic++;
      }
      this.rotate();
    },
    jumpNav(index) {
      clearInterval(this.rotateTimer);
      this.currentPic = index * 3;
      this.rotate();
    },
  },
};
</script>

<style lang="less" scoped>
.container {
  text-align: center;
  padding: 80px calc((100vw - 1100px) / 2);
  background: url(../../imgs/bg3.jpg) fixed;
  h3 {
    letter-spacing: 2px;
    font-size: 40px;
    font-family: "Montserrat-SemiBold", sans-serif;
    margin-bottom: 80px;
    color: #ffffff;
    span {
      color: #cc2105;
    }
  }
  .rotationContainer {
    width: 100%;
    overflow: hidden;
    .rotation {
      display: flex;
      justify-content: space-between;
      width: calc(350px * 9 + 160px);
      position: relative;
      transition: left 0.3s;
    }
    .switcher {
      margin-top: 20px;
      img {
        width: 20px;
        cursor: pointer;
        margin: 10px;
      }
    }
    .navPoint {
      margin-top: 20px;
      width: 100%;
      display: flex;
      justify-content: center;
      .point {
        margin: 5px;
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background: #c1bebe;
        &:hover {
          background: #ffffff;
        }
      }
    }
  }
}
</style>