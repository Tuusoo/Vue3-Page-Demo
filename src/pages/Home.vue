<template>
  <Page1 />
  <Page2 />
  <Page3 />
  <Page4 />
  <Page5 />
  <Page6 />
  <img
    src="../imgs/move-top.png"
    class="moveTop"
    v-show="!isTop"
    @click="scrollToTop"
  />
</template>

<script>
import Page1 from "../components/Page1/Page1.vue";
import Page2 from "../components/Page2/Page2.vue";
import Page3 from "../components/Page3/Page3.vue";
import Page4 from "../components/Page4/Page4.vue";
import Page5 from "../components/Page5/Page5.vue";
import Page6 from "../components/Page6/Page6.vue";

export default {
  name: "Home",
  components: {
    Page1,
    Page2,
    Page3,
    Page4,
    Page5,
    Page6,
  },
  data() {
    return {
      isTop: true,
      topDistance: 0,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScrollx);
  },
  methods: {
    handleScrollx() {
      this.topDistance = window.pageYOffset;
    },
    scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" });
    },
  },
  watch: {
    topDistance(val) {
      this.isTop = val > 200 ? false : true;
    },
  },
};
</script>

<style lang="less" scoped>
.moveTop {
  position: fixed;
  width: 30px;
  right: 60px;
  bottom: 30px;
  cursor: pointer;
}
</style>