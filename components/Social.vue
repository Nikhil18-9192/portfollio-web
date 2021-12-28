<template>
  <div id="social">
    <a-row type="flex" justify="center">
      <a-col :span="4">
        <a
          href="https://www.linkedin.com/in/dipak-korane-63b97a18b/"
          target="_blank"
        >
          <a-icon class="social-icon" type="linkedin" theme="filled" />
        </a>
      </a-col>
      <a-col :span="4">
        <a href="https://www.facebook.com/nikhil.korane.3/" target="_blank">
          <a-icon class="social-icon" type="facebook" theme="filled" />
        </a>
      </a-col>
      <a-col :span="4">
        <a
          href="https://www.instagram.com/nikhil_korane/?hl=en"
          target="_blank"
        >
          <a-icon class="social-icon" type="instagram" theme="filled" />
        </a>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  name: "SocialComponent",
};
</script>

<style lang="scss" scoped>
#social {
  position: absolute;
  bottom: 24px;
  width: 100%;
  a {
    text-decoration: none;
    color: $icon-color;
  }
  .social-icon {
    color: $icon-color;
    font-size: 18px;
    transition: 0.3s ease all;
    cursor: pointer;
    &:hover {
      color: $primary;
    }
  }
}
</style>