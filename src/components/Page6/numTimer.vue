<template>
  <span>{{ numChanger }}</span>
</template>

<script>
export default {
  props: {
    num: {
      type: Number,
      default: 2001,
      required: true,
    },
    isStart: {
      type: Boolean,
      default: false,
      required: true,
    },
  },
  data() {
    return {
      numChanger: 0,
      Timer: {},
    };
  },
  watch: {
    isStart(val) {
      if (val) {
        this.Timer = setInterval(() => {
          this.numChanger += parseInt(this.num / 100);
        }, 10);
        setTimeout(() => {
          this.numChanger = this.num;
        }, 1000);
      } else {
        this.numChanger = 0;
        clearInterval(this.Timer);
      }
    },
    numChanger(val) {
      if (val + this.num / 100 > this.num) {
        clearInterval(this.Timer);
      }
    },
  },
  unmounted() {
    clearInterval(this.Timer);
  },
};
</script>