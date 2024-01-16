<template>
  <div>
    <!-- Options API -->
    <input type="text" placeholder="First Name" v-model="fName" />
    <input type="text" placeholder="Last Name" v-model="lName" />
    <h2>Options fullName is {{ fullName }}</h2>

    <!-- Composition Api -->
    <input type="text" placeholder="First Name" v-model="refFirstName" />
    <input type="text" placeholder="Last Name" v-model="refLastName" />
    <h2>Options fullName is {{ refFullName }}</h2>
  </div>
</template>

<script>
import { computed, ref } from "vue";
export default {
  name: "Computed",
  setup() {
    const refFirstName = ref("");
    const refLastName = ref("");

    const refFullName = computed(() => {
      return `${refFirstName.value} ${refLastName.value}`;
    });

    return {
      refFirstName,
      refLastName,
      refFullName,
    };
  },
  data() {
    return {
      fName: "",
      lName: "",
    };
  },
  computed: {
    fullName() {
      return `${this.fName} ${this.lName}`;
    },
  },
};
</script>

<style scoped>
</style>