<template>
  <h3 v-for="name in names" :key="name.firstName">
    <slot :user="name"></slot>
  </h3>
</template>

<script>
export default {
  name: "NameList",
  data() {
    return {
      names: [
        {
          firstName: "Rahim",
          lastName: "Khan",
        },
        {
          firstName: "Jashim",
          lastName: "Seikh",
        },
        {
          firstName: "Fatema",
          lastName: "Khatun",
        },
        {
          firstName: "Musabbir",
          lastName: "Hossain",
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>