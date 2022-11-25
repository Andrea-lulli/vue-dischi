<template>
  <!-- header  -->
  <div>
    <img src="../assets/logo.svg" alt="" />
  </div>
</template>

<script>
export default {
  name: "HeaderComp",
};
</script>

<style lang="scss" scoped>

//style header
div {
  background-color: rgba(46, 58, 70, 255);

  height: 7vh;
  align-items: center;
  display: flex;

  img {
    width: 100px;
    fill: rgba(30, 214, 95, 255) !important;
  }
}
</style>