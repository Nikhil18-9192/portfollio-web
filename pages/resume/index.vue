<template>
  <div id="resume">
    <PageHeading title="My Resume" />
    <Resume />
  </div>
</template>

<script>
export default {
  layout: "default",
};
</script>
<style lang="scss" scoped>
#resume {
  position: relative;
  max-width: 1040px;
  width: 90%;
  margin: 0 auto;
  height: 100%;
  min-height: 100vh;
}
</style>