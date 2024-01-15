<template>
  <div>
    <h2>{{ firstName }} {{ lastName }}</h2>
  </div>
</template>

<script>
import { reactive, toRefs } from "vue";
export default {
  name: "DemoTwo",
  setup() {
    const state = reactive({
      firstName: "Mahmudul",
      lastName: "Hasan",
    });

    setTimeout(() => {
      state.firstName = "Hasan";
      state.lastName = "Mahmudul";
    }, 2000);

    return toRefs(state);
  },
};
</script>

<style scoped>
</style>