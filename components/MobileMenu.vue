<template>
  <div id="mobile-menu">
    <div class="image">
      <img class="profile-image" src="/profile.jpeg" alt="profile image" />
    </div>
    <Navbar />
    <Social />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#mobile-menu {
  display: none;
  height: 100vh;
  background: $sidebar-bg;
  @include for-phone-only {
    display: block;
    width: 50%;
    position: fixed;
    transition: 0.3s ease all;
    left: 0;
    top: 0;
    z-index: 15;
  }
  .image {
    position: relative;
    width: 100%;
    height: 200px;
    .profile-image {
      width: 100%;
      height: 100%;
      // object-fit: contain;
      // background: $primary;
    }
    .profile-name {
      position: absolute;
      width: 100%;
      height: 44px;
      bottom: 0;
      background: $primary;
      opacity: 0.9;
      display: flex;
      align-items: center;
      justify-content: center;
      p {
        color: $white;
        font-size: 20px;
        font-weight: 700;
        margin: 0;
        text-transform: uppercase;
      }
    }
  }
}
</style>