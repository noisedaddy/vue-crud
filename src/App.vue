<template>
  <div id="app">
    <!-- <test msg="hello from app.vue test component"></test> -->
    <user></user>
  </div>
</template>

<script>
// import Test from './components/Test'
import User from './components/Users'

export default {
  name: 'App',
  components: {
    User
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
