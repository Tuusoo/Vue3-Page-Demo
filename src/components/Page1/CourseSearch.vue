<template>
  <div class="container">
    <div class="title">Courses Search</div>
    <div class="selectors">
      <div class="selectorName">Select Degree</div>
      <NSelect
        v-model="degree"
        :options="options"
        default-value="Master Degree"
      />
      <div class="selectorName">Category</div>
      <NSelect
        v-model="degree"
        :options="options"
        default-value="Master Degree"
      />
      <div class="selectorName">Subject</div>
      <NSelect
        v-model="degree"
        :options="options"
        default-value="Master Degree"
      />
    </div>
    <div class="redButton">Search</div>
  </div>
</template>

<script>
import { NSelect } from "naive-ui";

export default {
  name: "CourseSearch",
  components: {
    NSelect,
  },
  data() {
    return {
      degree: "",
      options: [
        { label: "Master Degree", value: "Master Degree" },
        { label: "HS diploma", value: "HS diploma" },
        { label: "Associate Degree", value: "Associate Degree" },
        { label: "Bachelor's Degree", value: "Bachelor's Degree" },
        { label: "GED", value: "GED" },
        { label: "Doctorate/Prof Degree", value: "Doctorate/Prof Degree" },
      ],
    };
  },
};
</script>

<style lang="less" scoped>
.container {
  width: 380px;
  height: 450px;
  background: #000000;
  position: absolute;
  transform: translateX(360px);
  bottom: -350px;
  padding: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  color: #ffffff;
  z-index: 1;
  .title {
    font-family: "Montserrat-SemiBold", sans-serif;
    font-size: 24px;
  }
  .selectors {
    width: 100%;
    font-size: 16px;
    .selectorName {
      margin-top: 10px;
      line-height: 30px;
    }
  }
  .redButton {
    width: 100%;
    height: 50px;
    line-height: 50px;
    text-align: center;
    border: #cc2105 2px solid;
    color: #cc2105;
    border-radius: 2px;
    letter-spacing: 0.5px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s;
    &:hover {
      color: #ffffff;
      background: #cc2105;
    }
  }
}
</style>