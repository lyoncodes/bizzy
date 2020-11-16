<template>
  <div id="app">
    <!-- <img alt="Vue logo" class="header-logo" src="./assets/money-rocket.svg">\ -->
    <Header/>
    <NavTabs msg="Hi, I'm Michael"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import NavTabs from './components/NavTabs.vue'

export default {
  name: 'App',
  components: {
    Header,
    NavTabs
  }
}
</script>

<style lang="scss">
html {box-sizing: border-box;}
*,
*::before,
*::after {
  box-sizing: inherit;
}
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
