<template lang="pug">
  b-container
    div
      transition(name="fade" v-if="toggle")
        b-row
          b-col.col-4.mt-5
            b-row.justify-content-center
              h2.heading-a Link 1
            b-row
              b-col.mt-3
                a.anchor-a Link 2
                a.anchor-a Link 3
                a.anchor-a Link 4
                a.anchor-a Link 5
          b-col.col-4.mt-5
            b-row.justify-content-center
              h2.heading-a Link 1
            b-row
              b-col.mt-3
                a.anchor-a Link 2
                a.anchor-a Link 3
                a.anchor-a Link 4
                a.anchor-a Link 5
          b-col.col-4.mt-5
            b-row.justify-content-center
              h2.heading-a Link 1
            b-row
              b-col.mt-3
                a.anchor-a Link 2
                a.anchor-a Link 3
                a.anchor-a Link 4
                a.anchor-a Link 5
</template>
<script>
export default {
  name: 'profileMenu',
  props: ['toggle'],
  data () {
    return {
    }
  }
}
</script>
<style scoped lang="scss">
  .heading-a{
    padding-bottom: .25em;
    border-bottom: 1px solid orangered;
  }
  .anchor-a{
    color: black;
    display: block;
    font-size: 16pt;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
</style>