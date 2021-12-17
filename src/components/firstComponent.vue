<template>
  <div class="hello">
    <h1>{{ heading }}</h1>
      <p>Oefen project</p>
    <h3>Unordered list</h3>
    <ul>
      <li v-for="item in list" :key="item">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'firstComponent',
  props:
    ['heading', 'list']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
