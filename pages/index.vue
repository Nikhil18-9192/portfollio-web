<template>
  <div id="home">
    <Home />
  </div>
</template>

<script>
export default {
  layout: "default",
};
</script>
<style lang="scss" scoped>
#home {
  position: relative;
  width: 100%;
  height: 100vh;
  background-image: url("/bg.jpeg");
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
  max-height: 100vh;
  overflow: hidden;
}
</style>
