<template>
  <div>
    <input type="text" placeholder="reactive First Name" v-model="fName" />
    <input type="text" placeholder="reactive last Name" v-model="lName" />
    <input
      type="text"
      placeholder="reactive Hero Name"
      v-model="options.heroName"
    />
  </div>
</template>

<script>
import { ref, watch, reactive, toRefs } from "vue";
import _ from "lodash";
export default {
  name: "WatchReactive",
  setup() {
    const state = reactive({
      fName: "",
      lName: "",
      options: {
        heroName: "",
      },
    });

    // watch(
    //   () => {
    //     return { ...state };
    //   },
    //   (newValue, oldValue) => {
    //     console.log("fname oldvalue", oldValue.fName);
    //     console.log("fname newvalue", newValue.fName);
    //     console.log("lname oldvalue", oldValue.lName);
    //     console.log("lname oldvalue", newValue.lName);
    //   }
    // );

    watch(
      () => {
        return _.cloneDeep(state.options);
      },
      (newValue, oldValue) => {
        console.log("fname oldvalue", oldValue);
        console.log("fname newvalue", newValue);
      },
      {
        deep: true,
      }
    );

    return {
      ...toRefs(state),
    };
  },
};
</script>

<style scoped>
</style>