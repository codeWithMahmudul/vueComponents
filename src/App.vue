<template>
  <WatchReactive />
</template>

<script>
import WatchReactive from "./components/WatchReactive.vue";
export default {
  name: "App",
  components: {
    WatchReactive,
  },
};
</script>

<style>
VModel #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
