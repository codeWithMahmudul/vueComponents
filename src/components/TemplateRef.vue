<template>
  <div>
    <input type="text" ref="templateRef" />
    <Posts ref="postListRef" />
  </div>
</template>

<script>
import Posts from "./Posts.vue";
export default {
  name: "TemplateRef",
  components: {
    Posts,
  },
  mounted() {
    console.log(this.$refs.postListRef);
    this.$refs.templateRef.focus();
  },
};
</script>

<style lang="scss" scoped>
</style>