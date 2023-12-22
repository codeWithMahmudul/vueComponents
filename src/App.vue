<template>
  <ChildStyle />
  <h2>App conponent text</h2>
</template>

<script>
import ChildStyle from "./components/ChildStyle.vue";

export default {
  name: "App",
  components: {
    ChildStyle,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h2 {
  color: orange;
}
</style>
