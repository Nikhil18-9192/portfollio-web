<template>
  <div id="social">
    <a-row type="flex" justify="center">
      <a-col :span="4">
        <a href="#">
          <a-icon class="social-icon" type="linkedin" theme="filled" />
        </a>
      </a-col>
      <a-col :span="4">
        <a href="#">
          <a-icon class="social-icon" type="facebook" theme="filled" />
        </a>
      </a-col>
      <a-col :span="4">
        <a href="#">
          <a-icon class="social-icon" type="instagram" theme="filled" />
        </a>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#social {
  position: absolute;
  bottom: 24px;
  width: 100%;
  a {
    text-decoration: none;
    color: #777;
  }
  .social-icon {
    color: #777;
    font-size: 18px;
    cursor: pointer;
  }
}
</style>