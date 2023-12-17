<template>
  <h2>{{ name }}</h2>
  <h2>Test</h2>
  <h2>Test3</h2>  
  
  ddddd
  <ComponentC />
</template>

<script>
import ComponentC from './components/ComponentC.vue'

export default {
  name: 'App',
  components: {
    ComponentC
  },
  data() {
    return {
      name: 'mahmudul209307'
    }
  },
  provide() {
    return {
      username: this.name,
      name: "Mahmudul"
    }
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
