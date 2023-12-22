<template>
  <NameList>
    <template v-slot:default="slotProps">
      {{ slotProps.user.firstName }} {{ slotProps.user.lastName }}
    </template>
  </NameList>
</template>

<script>
import NameList from "./components/NameList.vue";

export default {
  name: "App",
  components: {
    NameList,
  },
  data() {
    return {};
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
