<template>
  <div>
    <h2>Options - {{ o_firstname }}</h2>
    <h2>
      Composition - {{ c_firstname }} {{ c_lastname }} a.k.a {{ c_heroname }}
    </h2>
    <h2>Composition - {{ greethero }}</h2>
    <h2>
      Composition - {{ state.firstName }} {{ state.lastName }} a.k.a
      {{ state.heroName }}
    </h2>
    <h2>Composition {{ reactieGreetHero }}</h2>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "Data",
  setup() {
    const c_firstname = ref("Diana");
    const c_lastname = ref("kent");
    const c_heroname = ref("Superman");
    const greet = `Hello ${c_firstname.value}`;
    const greethero = `Hello ${c_firstname.value} ${c_lastname.value} a.k.a ${c_heroname.value}`;

    const state = reactive({
      firstName: "Princess",
      lastName: "Diana",
      heroName: "Wonder Woman",
    });

    const reactieGreetHero = `Hello ${state.firstName} ${state.lastName} a.k.a ${state.heroName}`;
    return {
      c_firstname,
      c_lastname,
      c_heroname,
      greet,
      greethero,
      state,
      reactieGreetHero,
    };
  },
  data() {
    return {
      o_firstname: "Hasan",
    };
  },
};
</script>

<style scoped>
</style>