<template>
  <div>
    <h1 @mouseover="incrementCount">Hovered {{ count }} times</h1>
  </div>
</template>

<script>
import CounterMixin from "../mixins/counter";
export default {
  name: "HoverCounter",
  mixins: [CounterMixin],
};
</script>

<style scoped>
</style>