<template>
  <div>
    <!-- Option API -->
    <input type="text" placeholder="First Name" v-model="name" />

    <!-- Composition API -->
    <input type="text" placeholder="First Name" v-model="firstName" />
    <input type="text" placeholder="last Name" v-model="lastName" />
  </div>
</template>

<script>
import { ref, watch } from "vue";
export default {
  name: "Watch",
  setup() {
    const firstName = ref("");
    const lastName = ref("Hasan");

    watch(
      [firstName, lastName],
      (newValues, oldValues) => {
        console.log("Firstname New Value: ", newValues[0]);
        console.log("First Name Old Value: ", oldValues[0]);
        console.log("last name New Value: ", newValues[1]);
        console.log("last Name Old Value: ", oldValues[1]);
      },
      {
        immediate: true,
      }
    );

    return {
      firstName,
      lastName,
    };
  },
  data() {
    return {
      name: "",
    };
  },
  watch: {
    name(newValue, oldValue) {
      console.log("new Value: ", newValue);
      console.log("Old value: ", oldValue);
    },
  },
};
</script>

<style scoped>
</style>