<template>
  <div>
    <h2>{{ name }}</h2>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "DemoOne",
  setup() {
    let name = ref("Mahmudul Hasan");

    setTimeout(() => {
      name.value = "Hasan Mahmudul";
      console.log(name);
    }, 2000);

    return {
      name,
    };
  },
};
</script>

<style scoped>
</style>