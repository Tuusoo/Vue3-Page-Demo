<template>
  <div class="container">
    <div class="leftarea">
      <div class="title">Feel Free to Contact Our<br />Agents Directly</div>
      <div class="text">
        Nulla pellentesque mi non laoreet eleifend. Integer porttitor mollisar
        lorem, at molestie arcu pulvinar ut. Proin ac fermentum est. Cras mi
        ipsum, consectetur ac ipsum in, egestas vestibulum tellus.Proin ac
        fermentum est. Cras mi ipsum, consectetur ac ipsum in, egestas
        vestibulum tellus.
      </div>
      <div class="button">Read More</div>
    </div>
    <div class="rightarea">
      <div class="row1">
        <Card imageName="earth" />
        <Card imageName="hat" />
      </div>
      <div class="row2">
        <Card imageName="book" />
        <Card imageName="earth" />
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  components: {
    Card,
  },
};
</script>

<style lang="less" scoped>
.container {
  background: url(../../imgs/bg2.jpg) fixed;
  background-size: 100%;
  display: flex;
  justify-content: space-between;
  padding: 0 calc((100vw - 1100px) / 2);
  .leftarea {
    width: 50%;
    color: #ffffff;
    margin: 100px 0 200px 0;
    .title {
      font-family: "Montserrat-SemiBold", sans-serif;
      font-size: 26px;
      letter-spacing: 2px;
      font-weight: 600;
      line-height: 1.4em;
    }
    .text {
      font-size: 15px;
      line-height: 1.8em;
      letter-spacing: 1px;
      margin-top: 20px;
    }
    .button {
      background: #cc2105;
      border-radius: 3px;
      letter-spacing: 1px;
      font-size: 16px;
      line-height: 40px;
      height: 40px;
      width: 150px;
      text-align: center;
      margin-top: 20px;
      transition: background-color 0.3s;
      cursor: pointer;
      user-select: none;
      &:hover {
        background-color: #ef9632;
      }
    }
  }
  .rightarea {
    display: flex;
    margin-left: 50px;
    .row1 {
      margin: 40px 0 60px 0;
    }
    .row2 {
      margin-left: 30px;
    }
  }
}
</style>