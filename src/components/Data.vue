<template>
  <div>
    <h2>Options - {{ o_firstname }}</h2>
    <h2>Composition - {{ c_firstname }}</h2>
    <h2>Composition - {{ greet }}</h2>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Data",
  setup() {
    const c_firstname = ref('Diana');
    c_firstname.value = 'Clark'
    const greet = `Hello ${c_firstname.value}`
    console.log('c_firstname', c_firstname)
    return {
      c_firstname,
      greet
    };
  },
  data() {
    return {
      o_firstname: "Hasan",
    };
  },
};
</script>

<style scoped>
</style>