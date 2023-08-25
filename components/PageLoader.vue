<template>
  <div class="page-loader">
    <v-progress-circular size="50" indeterminate color="secondary"></v-progress-circular>
  </div>
</template>

<script>
export default {
  name: "PageLoader"
};
</script>

<style scoped>
.page-loader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.941);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}
</style>
