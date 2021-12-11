<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <p>{{ heading }} en {{ computeProp }}</p>
  <p>calculate this: {{calculate()}}</p>
  <div v-html="html"></div>
  <HelloWorld v-bind:list="list" v-bind:heading="heading"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      heading: 'Heading',
      html: '<h2>HTML content uit dataset</h2>',
      list: ['Een', 'Twee']
    }
  },
  computed: {
     computeProp: {
        get() {
        return this.heading && 'computedProp';
      }
     }
  },
  methods: {
    calculate() {
      return 1 + 2;
    }
  },
  components: {
    HelloWorld
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
