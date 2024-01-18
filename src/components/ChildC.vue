<template>
  <div>
    <h2>Child Component C</h2>
    <h2>Child Component C username {{ username }}</h2>
    <h2>Child Component composition C username {{ name }}</h2>
  </div>
</template>

<script>
import {inject} from 'vue'
export default {
  name: "ChildC",
  setup() {
    const name = inject('c_username', 'default username')

    return {
        name
    }
  },
  inject: ["username"],
};
</script>

<style scoped>
</style>