<template lang="pug">
  div.justify-content-center
    img.WordCloud-logo.mb-4(src="../assets/portrait.svg")
    h1 Michael Lyon
    div
      transition-group.wordCloud-container(name="flip")
        span(
          v-for="word in links" 
          :key="word"
          @click="toggleMenu")
            <router-link :to="word.href"> {{word.text}} </router-link>
    img.ux-i(src="../assets/Tap.svg" @click="magic")
</template>
<script>
export default {
  name: 'WordCloud',
  props: ['toggle'],
  data () {
    return {
      dept: [
        {text: 'markerting campaign', href: '#'},
        {text: 'small business', href: '#'},
        {text: 'product marketing', href: '#'},
        {text: 'event promotion', href: '#'},
        {text: 'webinar', href: '#'},
        {text: 'sales team', href: '#'},
        {text: 'ad campaign', href: '#'},
        {text: 'brand revamp', href: '#'},
        {text: 'online store', href: '#'},
        {text: 'social media', href: '#'},
      ],
      links: [
        {text: '', href: ''}, 
        {text: 'for your', href: ''}, 
        {text: '', href: ''},
      ],
      skillsLinks: [
        {text: 'animations', href: '#'}, 
        {text: 'responsive web pages', href: '#'}, 
        {text: 'one-pagers', href: '#'}, 
        {text: 'trademarks & logos', href: '#'}, 
        {text: 'frontend forms', href: '#'}, 
        {text: 'email templates', href: '#'}, 
        {text: 'CRM integrations', href: '#'}, 
        {text: 'landing pages', href: '#'},
        {text: 'mobile-first', href: '#'},
        {text: 'creative ideas', href: '#'},
      ],
      showList: null,
    }
  },
  mounted() {
    this.magic();
  },
  methods: {
    magic() {
      let newLinks = [...this.links];
      newLinks[0] = this.getRandom();
      newLinks[2] = this.getAnotherRandom();
      this.links = newLinks;
    },
    getRandom () {
      let rndIdx = Math.floor(Math.random() * this.skillsLinks.length);
      return this.skillsLinks[rndIdx]
    },
    getAnotherRandom () {
      let rndIdx = Math.floor(Math.random() * this.dept.length);
      return this.dept[rndIdx]
    },
    toggleMenu () {
      this.showList = !this.showList
      this.$emit('toggleSkillsList', this.showList)
    }
  },
}
</script>
<style scoped lang="scss">
  .WordCloud-logo {
    height: 250px;
    margin-left: 3em;
  }
  .ux-i{
    margin: 3em auto;
    height: 50px;
    position: absolute;
    left: 33%;
    top: 65%;
  }
  .wordCloud-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  text-align: center;
  font-size: 30px;

    & > * {
      transition: 1s ease;
      margin: 0 0.2em;
    }
    a {
      color: orange !important;
    }
  }
  .flip-enter,
  .flip-leave-to {
    opacity: 0;
    transform: scale(0);
  }
  .flip-leave-active {
    position: absolute;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s;
  }
</style>