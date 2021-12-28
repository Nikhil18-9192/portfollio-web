<template>
  <div>
    <a-row>
      <a-col :span="3">
        <Sidebar />
      </a-col>
      <a-col :span="21">
        <div class="page-container">
          <Nuxt />
        </div>
      </a-col>
    </a-row>
  </div>
</template>

<script>
import Sidebar from "~/components/Sidebar.vue";
export default {
  components: { Sidebar },
};
</script>

<style lang="scss" scoped>
body {
  font-family: "Roboto Mono", monospace;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
.page-container {
  width: 100%;
  background: $bg;
  max-height: 100vh;
  overflow-y: scroll;
  &::-webkit-scrollbar {
    width: 6px;
    border-radius: 2.5px;
  }
  &::-webkit-scrollbar-track {
    background: $bg;
    border-radius: 2.5px;
  }
  &::-webkit-scrollbar-thumb {
    background: $sidebar-bg;
    border-radius: 2.5px;
  }
}
h1,
h2,
h3,
h4,
h5,
p {
  padding: 0;
  margin: 0;
}

.my-page-enter,
.my-page-leave-active {
  transition: 0.3s ease all;
  opacity: 0;
  // transform: translateX(-100px);
  transform-origin: center;
  transform: scale(1.02);
}
</style>