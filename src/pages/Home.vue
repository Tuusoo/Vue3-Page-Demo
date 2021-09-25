<template>
  <Page1 />
  <Page2 />
  <Page3 />
</template>

<script>
import Page1 from "../components/Page1/Page1.vue";
import Page2 from "../components/Page2/Page2.vue";
import Page3 from "../components/Page3/Page3.vue";

export default {
  name: "Home",
  components: {
    Page1,
    Page2,
    Page3,
  },
};
</script>