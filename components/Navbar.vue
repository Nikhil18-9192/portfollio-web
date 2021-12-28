<template>
  <div class="navbar">
    <nuxt-link
      v-for="item in navItem"
      :key="item.name"
      :to="item.route"
      class="nav"
    >
      <a-icon class="nav-icon" type="home" v-if="item.name === 'Home'" />
      <a-icon class="nav-icon" type="user" v-if="item.name === 'About Me'" />
      <a-icon class="nav-icon" type="profile" v-if="item.name === 'Resume'" />
      <a-icon
        class="nav-icon"
        type="project"
        v-if="item.name === 'Portfolio'"
      />
      <a-icon class="nav-icon" type="mail" v-if="item.name === 'Contact Me'" />
      {{ item.name }}
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      navItem: [
        { name: "Home", route: "/" },
        { name: "About Me", route: "/aboutMe" },
        { name: "Resume", route: "/resume" },
        { name: "Portfolio", route: "/portfolio" },
        { name: "Contact Me", route: "/contactMe" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  position: relative;
  width: 100%;

  .nav {
    position: relative;
    display: flex;
    flex-direction: column;
    padding: 12px 0 12px 70px;
    height: 45px;
    text-transform: uppercase;
    color: #777;
    border-bottom: 1px solid #202226;
    font-size: 12px;
    .nav-icon {
      position: absolute;
      left: 35px;
      top: 11px;
      font-size: 20px;
    }
  }
  .nuxt-link-exact-active {
    color: #fff !important;
  }
}
</style>