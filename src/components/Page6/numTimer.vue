<template>
  <span>{{ numChanger }}</span>
</template>

<script>
export default {
  props: {
    num: Number,
    isStart: Boolean,
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
      }
    },
    numChanger(val) {
      if (val + this.num / 100 > this.num) {
        clearInterval(this.Timer);
      }
    },
  },
};
</script>