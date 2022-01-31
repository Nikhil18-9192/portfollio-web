<template>
  <div class="sidebar">
    <div class="image">
      <img class="profile-image" src="/profile.jpeg" alt="profile image" />
      <div class="profile-name">
        <p>Deepak Korane</p>
      </div>
    </div>
    <Navbar />
    <Social />
  </div>
</template>

<script>
export default {
  name: "sidebar",
};
</script>

<style lang="scss" scoped>
.sidebar {
  position: relative;
  width: 100%;
  height: 100vh;
  background: $sidebar-bg;
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