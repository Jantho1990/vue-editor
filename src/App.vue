<template>
  <div id="app">
    <simple-demo></simple-demo>
  </div>
</template>

<script>
import SimpleDemo from './SimpleDemo'

export default {
  name: 'App',
  components: {
    SimpleDemo
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
