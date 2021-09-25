<template>
  <Home></Home>
</template>

<script>
import Home from "./pages/Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: "Roboto-Regular", sans-serif;
}

div {
  box-sizing: border-box;
}

.n-base-selection .n-base-selection-label {
  background: transparent;
}

.n-base-selection:not(.n-base-selection--disabled).n-base-selection--active
  .n-base-selection-label {
  background: transparent;
}

.n-base-selection
  .n-base-selection-label
  .n-base-selection-input
  .n-base-selection-input__content {
  color: #ffffff;
  font-family: "Roboto-Regular", sans-serif;
  font-size: 16px;
}

@font-face {
  font-family: "Montserrat-Bold";
  src: url(./fonts/Montserrat-Bold.ttf);
}

@font-face {
  font-family: "Montserrat-SemiBold";
  src: url(./fonts/Montserrat-SemiBold.ttf);
}

@font-face {
  font-family: "Montserrat-Medium";
  src: url(./fonts/Montserrat-Medium.ttf);
}

@font-face {
  font-family: "Roboto-Bold";
  src: url(./fonts/Roboto-Bold.ttf);
}

@font-face {
  font-family: "Roboto-Regular";
  src: url(./fonts/Roboto-Regular.ttf);
}
</style>
