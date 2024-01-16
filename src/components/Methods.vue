<template>
  <div>
    <h2>{{ name }}</h2>
    <button @click="setName">Change Name</button>

    <h2>{{ count }}</h2>
    <button @click="incrementCount">incrementCount</button>

    <h2>{{ firstName }} {{ lastName }}</h2>
    <button @click="changeName">Change name</button>
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";
export default {
  name: "Methods",
  setup() {
    const count = ref(0);
    function incrementCount() {
      count.value++;
    }

    const state = reactive({
      firstName: "Mahmudul",
      lastName: "Hasan",
    });

    function changeName() {
      state.firstName = "Bruce";
      state.lastName = "Lee";
    }

    return {
      count,
      incrementCount,
      ...toRefs(state),
      changeName,
    };
  },
  data() {
    return {
      name: "viswas",
    };
  },
  methods: {
    setName() {
      this.name = "Mahmudul Hasan";
    },
  },
};
</script>

<style scoped>
</style>