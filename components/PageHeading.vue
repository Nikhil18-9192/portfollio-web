<template>
  <div id="page-heading">
    <h2>{{ title }}.</h2>
    <a-icon class="heading-icon" type="user" v-if="title === 'About Me'" />
    <a-icon class="heading-icon" type="profile" v-if="title === 'My Resume'" />
    <a-icon class="heading-icon" type="project" v-if="title === 'Portfolio'" />
    <a-icon class="heading-icon" type="mail" v-if="title === 'Contact Me'" />
  </div>
</template>

<script>
export default {
  name: "PageHeading",
  props: ["title"],
};
</script>

<style lang="scss" scoped>
#page-heading {
  position: relative;
  width: 100%;
  border-bottom: 1px dashed rgba(255, 255, 255, 0.2);
  margin-bottom: 50px;
  padding-top: 50px;
  display: flex;
  justify-content: space-between;
  h2 {
    color: #00a3e1;
    font-size: 36px;
    font-weight: 700;
    letter-spacing: 1.5px;
    line-height: 1em;
    text-transform: capitalize;
    font-family: "Playfair Display", serif;
  }
  .heading-icon {
    font-size: 38px;
    line-height: 1em;
    color: #00a3e1;
  }
}
</style>