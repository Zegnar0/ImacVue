<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  data() {
    return {
      title: "Space X Rockets Checker",
    };
  },
};
</script>

<style scoped>
header {
  background: linear-gradient(to bottom, rgba(51, 51, 51, 0.5), rgba(51, 51, 51, 0));
  color: #fff;
  padding: 10px;
  text-align: center;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
}
</style>
