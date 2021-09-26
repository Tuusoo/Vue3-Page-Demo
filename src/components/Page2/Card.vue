<template>
  <div
    :class="isHover ? 'card hover' : 'card'"
    @mouseover="changeStyle"
    @mouseout="changeStyle"
  >
    <img :src="isHover ? detail.image_blue : detail.image" />
    <div class="title">{{ detail.title }}</div>
    <div class="text">{{ detail.text }}</div>
  </div>
</template>

<script>
export default {
  props: {
    detail: Object,
  },
  data() {
    return {
      isHover: false,
    };
  },
  methods: {
    changeStyle() {
      this.isHover = !this.isHover;
    },
  },
};
</script>

<style lang="less" scoped>
.card {
  width: 30%;
  background: #edeeef;
  padding: 50px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  transition: background-color 0.3s;
  img {
    width: 40px;
  }
  .title {
    font-family: "Montserrat-Medium", sans-serif;
    font-size: 20px;
    margin-top: 20px;
    transition: color 0.3s;
  }
  .text {
    margin-top: 20px;
    width: 80%;
    color: #333;
    font-size: 15px;
    line-height: 2em;
    letter-spacing: 1px;
  }
  &.hover {
    background: #d6d6d6;
    .title {
      color: #ffffff;
    }
  }
}
</style>