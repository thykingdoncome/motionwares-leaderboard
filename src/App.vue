<template>
  <div id="app">
    <Dashboard />
  </div>
</template>

<script>
import Dashboard from './views/Dashboard'

export default {
  name: 'App',
  components: {
    Dashboard
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
