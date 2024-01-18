<template>
  <div>
    <h2>Parent Component</h2>
    <ChildA />
  </div>
</template>

<script>
import {provide, ref, reactive, torefs} from 'vue'
import ChildA from "./ChildA.vue";
export default {
  components: {
    ChildA,
  },
  name: "ProvideInject",
  setup(){
    provide('c_username', 'MahmudulHasan')
  },
  data() {
    return {
        name: 'Mahmudul'
    }
  },
  provide() {
    return {
        username: this.name,
    }
  }
};
</script>

<style scoped>
</style>