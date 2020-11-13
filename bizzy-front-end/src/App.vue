<template>
  <div id="app">
    <img alt="Vue logo" class="header-logo" src="./assets/money-rocket.svg">
    <HelloWorld msg="Hi, I'm Michael"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
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
.header-logo {
  height: 250px;
}
</style>
