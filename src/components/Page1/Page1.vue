<template>
  <div class="bg">
    <div class="bar">
      <div class="logo" @click="originalPage">
        SUBJECT
        <span>EDUCATION</span>
      </div>
      <div class="buttons">
        <div class="button">Home</div>
        <div class="button">About Us</div>
        <n-popselect
          v-model:value="chooseValue"
          trigger="click"
          :options="options"
        >
          <div class="button">
            Dropdown
            <img src="../../imgs/down.svg" />
          </div>
        </n-popselect>
        <div class="button">Contact Us</div>
      </div>
    </div>
    <div class="content">
      <div class="title">
        WHAT WOULD
        <span>YOU LIKE</span><br />
        TO LEARN?
      </div>
      <div class="button">Know More</div>
    </div>
    <CourseSearch />
  </div>
</template>

<script>
import { NPopselect } from "naive-ui";
import CourseSearch from "./CourseSearch.vue";

export default {
  name: "Page1",
  components: {
    NPopselect,
    CourseSearch,
  },
  data() {
    return {
      chooseValue: "",
      options: Object.freeze([
        { label: "Services", value: "Services" },
        { label: "Typography", value: "Typography" },
        { label: "Gallery", value: "Gallery" },
      ]),
    };
  },
  methods: {
    originalPage() {
      window.open(
        "http://www.cssmoban.com/preview/index.html?url=http://demo.kangjingept.com:8020/cssthemes6/oyqj-0907-1/index.html&id=27491&tid=20125072756579",
        "_blank"
      );
    },
  },
};
</script>

<style lang="less" scoped>
.bg {
  position: relative;
  background: url(../../imgs/bg1.jpg) center no-repeat;
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  user-select: none;

  .bar {
    position: absolute;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .logo {
      color: #ffffff;
      font-size: 38px;
      font-family: "Montserrat-Bold", sans-serif;
      font-weight: 700;
      letter-spacing: 2px;
      line-height: 1.2;
      text-align: center;
      display: flex;
      flex-direction: column;
      margin: 20px 0 0 80px;
      cursor: pointer;
      span {
        font-size: 6px;
        font-family: "Roboto-Bold", sans-serif;
        letter-spacing: 6px;
        text-align: center;
      }
    }
    .buttons {
      display: flex;
      justify-content: space-between;
      align-items: center;
      color: #ffffff;
      width: 400px;
      margin-right: 100px;
      .button {
        font-weight: 400;
        font-size: 15px;
        letter-spacing: 1px;
        cursor: pointer;
        height: 40px;
        line-height: 40px;
        box-sizing: border-box;
        img {
          width: 15px;
          margin-left: 3px;
          transform: translateY(3px);
        }
        &:first-child {
          border-bottom: 3px solid #cc2105;
        }
        &:hover {
          border-bottom: 3px solid #cc2105;
        }
      }
    }
  }
  .content {
    height: 90vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    .title {
      font-size: 60px;
      color: #fff;
      font-weight: 600;
      letter-spacing: 2px;
      text-align: center;
      line-height: 1.2;
      font-family: "Montserrat-SemiBold", sans-serif;
      span {
        color: #cc2105;
      }
    }
    .button {
      background: #cc2105;
      color: #fff;
      letter-spacing: 1px;
      height: 40px;
      width: 140px;
      border-radius: 3px;
      text-align: center;
      font-size: 16px;
      line-height: 40px;
      margin-top: 40px;
      transition: background-color 0.3s, transform 0.6s;
      cursor: pointer;
      &:hover {
        background: #0ebeff;
        transform: translateY(10px);
      }
    }
  }
}
</style>
