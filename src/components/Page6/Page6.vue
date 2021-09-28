<template>
  <div class="whitearea container">
    <h3>OUR <span>ACHIEVEMENTS</span></h3>
    <div class="items" ref="nums">
      <div class="item">
        <img src="../../imgs/champion.svg" />
        <div class="num"><NumTimer :num="num1" :isStart="isNumShow" /></div>
        <div class="text">Year of Foundation</div>
      </div>
      <div class="item">
        <img src="../../imgs/hat.svg" />
        <div class="num"><NumTimer :num="num2" :isStart="isNumShow" /></div>
        <div class="text">Graduates</div>
      </div>
      <div class="item">
        <img src="../../imgs/a_man.svg" />
        <div class="num"><NumTimer :num="num3" :isStart="isNumShow" /></div>
        <div class="text">Certified Staff</div>
      </div>
      <div class="item">
        <img src="../../imgs/3_man.svg" />
        <div class="num"><NumTimer :num="num4" :isStart="isNumShow" /></div>
        <div class="text">Students</div>
      </div>
    </div>
  </div>
  <div class="blackarea container">
    <div class="left">
      <h5>Get In Touch</h5>
      <div>0926k 4th block building,king Avenue,</div>
      <div>New York City,USA</div>
      <div>phone: +0444 555 6789</div>
      <div>Fax: +0444 555 6789</div>
      <div>Mail: <span>info@example.com</span></div>
    </div>
    <div class="left">
      <h5>About Us</h5>
      <div>
        Curabitur non nulla sit amet nislinit tempus convallis quis ac lectus.
        lac inia eget consectetur sed, convallis at tellus. Nulla porttitor
        accumsana tincidunt. Vestibulum ante ipsum primis tempus convallis.
      </div>
    </div>
    <div class="inputArea">
      <h5>Subscribe Our Newsletter</h5>
      <div class="input">
        <input type="email" placeholder="Email Address" />
        <div>SUBSCRIBE</div>
      </div>
    </div>
  </div>
  <div class="bottom container">
    <div class="text">😈 Plagiarized by Tuusoo~</div>
    <div class="icons">
      <div class="icon icon1" @mouseover="hover1" @mouseout="hover1">
        <img
          :src="
            icon1Hover
              ? require('../../imgs/icon1_color.svg')
              : require('../../imgs/icon1.svg')
          "
        />
      </div>
      <div class="icon icon2" @mouseover="hover2" @mouseout="hover2">
        <img
          :src="
            icon2Hover
              ? require('../../imgs/icon2_color.svg')
              : require('../../imgs/icon2.svg')
          "
        />
      </div>
      <div class="icon icon3" @mouseover="hover3" @mouseout="hover3">
        <img
          :src="
            icon3Hover
              ? require('../../imgs/icon3_color.svg')
              : require('../../imgs/icon3.svg')
          "
        />
      </div>
      <div class="icon icon4" @mouseover="hover4" @mouseout="hover4">
        <img
          :src="
            icon4Hover
              ? require('../../imgs/icon4_color.svg')
              : require('../../imgs/icon4.svg')
          "
        />
      </div>
    </div>
  </div>
</template>

<script>
import NumTimer from "./numTimer.vue";

export default {
  name: "Page6",
  components: {
    NumTimer,
  },
  data() {
    return {
      icon1Hover: false,
      icon2Hover: false,
      icon3Hover: false,
      icon4Hover: false,
      isNumShow: false,
      num1: 2001,
      num2: 765,
      num3: 125,
      num4: 150,
    };
  },
  mounted() {
    const numsObserver = new IntersectionObserver((items) => {
      items.forEach((item) => {
        console.log(item);
        if (item.intersectionRatio > 0) {
          this.isNumShow = true;
        } else {
          this.isNumShow = false;
        }
      });
    });
    numsObserver.observe(this.$refs.nums);
  },
  methods: {
    hover1() {
      this.icon1Hover = !this.icon1Hover;
    },
    hover2() {
      this.icon2Hover = !this.icon2Hover;
    },
    hover3() {
      this.icon3Hover = !this.icon3Hover;
    },
    hover4() {
      this.icon4Hover = !this.icon4Hover;
    },
  },
};
</script>

<style lang="less" scoped>
.container {
  padding-left: calc((100vw - 1100px) / 2);
  padding-right: calc((100vw - 1100px) / 2);
}
.whitearea {
  text-align: center;
  padding-top: 80px;
  padding-bottom: 80px;
  h3 {
    letter-spacing: 2px;
    font-size: 40px;
    font-family: "Montserrat-SemiBold", sans-serif;
    span {
      color: #cc2105;
    }
  }
  .items {
    display: flex;
    justify-content: space-between;
    margin-top: 80px;
    .item {
      display: flex;
      flex-direction: column;
      align-items: center;
      img {
        width: 40px;
        height: 40px;
      }
      div {
        margin-top: 10px;
        &.num {
          font-size: 40px;
          letter-spacing: 2px;
          color: #2e1f54;
          font-family: "Roboto-Bold", sans-serif;
        }
        &.text {
          font-size: 18px;
          letter-spacing: 1px;
          font-family: "Montserrat-Medium", sans-serif;
        }
      }
    }
  }
}
.blackarea {
  background: #101010;
  display: flex;
  padding-top: 60px;
  padding-bottom: 100px;
  h5 {
    font-size: 27px;
    letter-spacing: 2px;
    color: #ffffff;
    font-family: "Montserrat-Regular", sans-serif;
    margin-bottom: 60px;
  }
  .left {
    width: 25%;
    padding-right: 20px;
    div {
      color: #bbbbbb;
      line-height: 28px;
      font-size: 15px;
      letter-spacing: 0.7px;
      span {
        color: #cc2105;
      }
    }
  }
  .inputArea {
    width: 50%;
    padding-left: 20px;
    .input {
      display: flex;
      input {
        height: 50px;
        width: 70%;
        border-radius: 3px;
        border: 0;
        padding-left: 20px;
        box-sizing: border-box;
        letter-spacing: 1px;
        outline: none;
        &:focus {
          border: 2px solid #00a2d8;
        }
      }
      div {
        height: 50px;
        width: calc(30% - 10px);
        margin-left: 5px;
        background: #cc2105;
        border-radius: 3px;
        display: inline-block;
        color: #ffffff;
        text-align: center;
        line-height: 50px;
        font-size: 18px;
        user-select: none;
        cursor: pointer;
        transition: background-color 0.3s;

        &:hover {
          background-color: #ef9632;
        }
      }
    }
  }
}
.bottom {
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #000000;
  .text {
    color: #333;
    font-size: 15px;
    line-height: 1.8;
    letter-spacing: 1px;
  }
  .icons {
    display: flex;
    .icon {
      border: 2px solid #ffffff;
      border-radius: 50%;
      margin-left: 10px;
      width: 35px;
      height: 35px;
      display: flex;
      align-items: center;
      justify-content: center;
      &.icon1:hover {
        border-color: #667eb9;
      }
      &.icon2:hover {
        border-color: #5dd7fc;
      }
      &.icon3:hover {
        border-color: #f35e47;
      }
      &.icon4:hover {
        border-color: #38a6d9;
      }
      img {
        width: 16px;
      }
    }
  }
}
</style>