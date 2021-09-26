<template>
  <div class="card">
    <h5>Tempor incididunt ut labore hytnm</h5>
    <div class="text">
      Lorem ipsum dolor sit amet consectetur adipisicing elit sedc dnmo.
    </div>
    <div class="data">
      <img :src="person.image" alt="headpic" />
      <div>{{ person.name }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    person: Object,
  },
  // computed: {
  //   pic() {
  //     switch(this.personName){
  //       case "Mary Jane":
  //         return require("../../imgs/te1.jpg");
  //       case "Olivia Ruth":
  //         return require("../../imgs/te3.jpg");
  //       case "Blake Joe":
  //         return require("../../imgs/te2.jpg");
  //       case ""
  //     }
  //   }
  // }
};
</script>

<style lang="less" scoped>
.card {
  width: 350px;
  height: 330px;
  background: #ffffff;
  padding: 50px 30px;
  text-align: left;
  h5 {
    font-family: "Montserrat-Regular", sans-serif;
    color: #212529;
    line-height: 1.2;
    font-size: 24px;
    letter-spacing: 1px;
  }
  .text {
    color: #333;
    font-size: 15px;
    line-height: 1.8;
    letter-spacing: 1px;
    margin-top: 10px;
  }
  .data {
    display: flex;
    align-items: center;
    margin-top: 20px;
    img {
      width: 25%;
      border-radius: 50%;
    }
    div {
      font-family: "Montserrat-SemiBold", sans-serif;
      color: #504e4e;
      font-size: 17px;
      letter-spacing: 1px;
      margin-left: 20px;
    }
  }
}
</style>