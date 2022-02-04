<template>
  <div class="home-bg">
    <div class="blur"></div>
    <div class="title">
      <h1>Deepak <span>Korane</span></h1>
      <p class="sub-text">I am a <span>Front-end Developer</span></p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.home-bg {
  position: relative;
  width: 100%;
  height: 100vh;
  .blur {
    position: absolute;
    width: 100%;
    height: 100%;
    backdrop-filter: blur(1px);
    background: rgba(0, 0, 0, 0.493);
    z-index: 1;
  }
  .title {
    z-index: 10;
    position: absolute;
    left: 50%;
    top: 35%;
    transform: translate(-50%, 0);

    h1 {
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 62px;
      font-weight: 500;
      color: #fff;
      margin-bottom: 0;
      span {
        color: #00a3e1;
      }
    }
    .sub-text {
      color: #fff;
      font-size: 30px;
      font-weight: 400;
      text-align: center;
      span {
        font-weight: 700;
      }
    }
  }
}
</style>