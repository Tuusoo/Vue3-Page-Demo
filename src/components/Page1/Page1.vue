<template>
  <div class="bg">
    <div class="bar">
      <div class="logo">
        SUBJECT
        <span>EDUCATION</span>
      </div>
      <div class="buttons">
        <div class="button">Home</div>
        <div class="button">About Us</div>
        <div class="button">Dropdown</div>
        <div class="button">Contact Us</div>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
.bg {
  background: url(../../imgs/bg1.jpg) center no-repeat;
  background-size: cover;
  
  .bar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .logo {
      color: #FFFFFF;
      font-size: 38px;
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      letter-spacing: 2px;
      text-align: center;
      display: flex;
      flex-direction: column;
      margin: 20px 0 0 80px;
      user-select: none;
      cursor: pointer;
      span {
        font-size: 8px;
        font-family: 'Roboto', sans-serif;
        letter-spacing: 6px;
        text-align: center;
      }
    }
    .buttons {
      display: flex;
      align-items: center;
      color: #FFFFFF;
    }
  }
}
</style>