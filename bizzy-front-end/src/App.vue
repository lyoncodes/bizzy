<template lang="pug">
  #app
    <router-view/>
    //- WordCloud(
    //-   v-on:toggleSkillsList="toggleLinkList($event)"
    //- )
    b-row
      ProfileMenu(
        :toggle="toggleBoolean"
      )
</template>

<script>
import WordCloud from './components/WordCloud.vue'
import NavTabs from './components/NavTabs.vue'
import ProfileMenu from './components/ProfileMenu'
export default {
  name: 'App',
  data () {
    return {
      toggleBoolean: false
    }
  },
  methods: {
    toggleLinkList (booleanData) {
      this.toggleBoolean = booleanData
    }
  },
  components: {
    WordCloud,
    NavTabs,
    ProfileMenu
  }
}
</script>

<style lang="scss">
html {
  box-sizing: border-box
}
*,
*::before,
*::after {
  box-sizing: inherit;
}
body {
  overflow: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px
}
</style>
