<template>
  <div class="container">
    <h3>OUR <span>ADVANTAGES</span></h3>
    <div class="row">
      <div class="image">
        <img src="../../imgs/p1.jpg" alt="p1.jpg" class="round" />
      </div>
      <div class="textarea">
        <h6>INTEGER PORTTITOR MOLLISAR</h6>
        <h5>Laoreet Eleifend</h5>
        <div>
          Nulla pellentesque mi non laoreet eleifend. Integer porttitor mollisar
          lorem, at molestie arcu pulvinar ut. Proin ac fermentum est. Cras mi
          ipsum, consectetur ac ipsum in, egestas vestibulum tellus.
        </div>
      </div>
    </div>
    <div class="row">
      <div class="textarea">
        <h6>INTEGER PORTTITOR MOLLISAR</h6>
        <h5>Pellentesque mi non</h5>
        <div>
          Nulla pellentesque mi non laoreet eleifend. Integer porttitor mollisar
          lorem, at molestie arcu pulvinar ut. Proin ac fermentum est. Cras mi
          ipsum, consectetur ac ipsum in, egestas vestibulum tellus.
        </div>
      </div>
      <img src="../../imgs/g1.jpg" alt="g1.jpg" class="square" />
    </div>
  </div>
</template>

<style lang="less" scoped>
.container {
  width: 1100px;
  margin-left: 50%;
  transform: translateX(-50%);
  text-align: center;
  padding: 80px 0;
  h3 {
    letter-spacing: 2px;
    font-size: 40px;
    font-family: "Montserrat-SemiBold", sans-serif;
    margin-bottom: 80px;
    span {
      color: #cc2105;
    }
  }
  .row {
    display: flex;
    justify-content: center;
    .image {
      width: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      .round {
        width: 270px;
        height: 270px;
        border-radius: 50%;
      }
    }

    .textarea {
      text-align: left;
      width: 50%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding-right: 30px;
      h6 {
        font-size: 15px;
        letter-spacing: 2px;
        color: #cc2105;
        font-family: "Montserrat-Bold", sans-serif;
      }
      h5 {
        font-size: 30px;
        letter-spacing: 2px;
        font-family: "Montserrat-Bold", sans-serif;
      }
      div {
        color: #333;
        font-size: 15px;
        line-height: 1.8;
        letter-spacing: 1px;
      }
    }
    .square {
      width: 50%;
    }
  }
}
</style>