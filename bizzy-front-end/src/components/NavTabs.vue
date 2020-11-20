<template>
  <div>
    <nav>
      <ul>
        <li>
          <a href="#">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span>
              <h5>Work</h5>
            </span>
          </a>
        </li>
        <li>
          <a href="#">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span>
              <h5>Blog</h5>
            </span>
          </a>
        </li>
        <li>
          <a href="#">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <span>
              <h5>CVV</h5>
            </span>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavTabs',
  data () {
    return {
      showWork: false
    }
  },
  mounted() {
    this.showWorkToggle();
  },
  methods: {
    showWorkToggle() {
      this.showWork = !this.showWork;
      this.$emit('toggleList', this.showWork)
    }
  }
}
</script>

<style scoped lang="scss">

h5 {
  color: #3b5998;
  font-size: .65em;
  padding: .5em;
}

a {
  text-decoration: none;
  color: #fff;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0 auto;
  width: 66vh;
  height: 33vh;
  display: flex;
  justify-content: center;
  transform-style: preserve-3d;
  transform: rotate(-25deg) skew(20deg);
}

ul li {
  position: relative;
  background-color: #f0f0f0;
  margin-right: 15px;
  width: 25%;
  transition: .4s;
}

ul li:last-of-type {margin-right: 0;}

ul li::before {
  content: '';
  position: absolute;
  top: 0;
  left: -9px;
  background-color: #b3b3b3;
  height: 100%;
  width: 9px;
  transform-origin: right;
  transform: skewY(-45deg);
}

ul li::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  background-color: #979797;
  width: 100%;
  height: 10px;
  transform-origin: top;
  transform: skewX(-45deg);
}

ul li span {
  position: absolute;
  top: 0;
  left: 0;
  display: flex !important;
  justify-content: center;
  align-items: center;
  color: rgba(255, 255, 255, .2);
  width: 100%;
  height: 100%;
  font-size: 3em;
  transition: .4s;
}

li:hover a span {
  z-index: 1000;
  transition: .5s;
  color: rgba(255, 255, 255, 1);
  box-shadow: -1px 1px 1px rgba(0, 0, 0, .05);
}

li:hover > a span:nth-of-type(1) {transform: translate(10px, -10px);}
li:hover > a span:nth-of-type(2) {transform: translate(20px, -20px);}
li:hover > a span:nth-of-type(3) {transform: translate(30px, -30px);}
li:hover > a span:nth-of-type(4) {transform: translate(40px, -40px);}
li:hover > a span:nth-of-type(5) {transform: translate(50px, -50px);}

a span:nth-of-type(1) {opacity: .2;}
a span:nth-of-type(2) {opacity: .4;}
a span:nth-of-type(3) {opacity: .6;}
a span:nth-of-type(4) {opacity: .8;}
a span:nth-of-type(5) {opacity: 1;}

li:nth-of-type(1):hover span {
  background-color: #d6249f;
  background-image: linear-gradient(270deg, #fd5949, #d6249f, #285aeb);
  background-size: 800% 800%;
  animation: gradient 10s ease infinite;
}
li:nth-of-type(1) h5 {
  color:#4cbdff;
  animation: gradient 10s ease infinite;
}
li:nth-of-type(1):hover h5 {
  color:#fd5949;
  animation: gradient 10s ease infinite;
}

li:nth-of-type(2):hover span {
  background-color: #3b5998;
  background-image: linear-gradient(270deg, #3b5998, #d31847);
  background-size: 400% 400%;
  animation: gradient 6s ease infinite;

}
li:nth-of-type(2) h5 {
  color:#fd5949;
  animation: gradient 6s ease infinite;
}
li:nth-of-type(2):hover h5 {
  color:#4cbdff;
  animation: gradient 6s ease infinite;
}

li:nth-of-type(3):hover span {
  background-color: #0077f2;
  background-image: linear-gradient(270deg, #4cbdff, #0077f2);
  background-size: 400% 400%;
  animation: gradient 6s ease infinite;
}
li:nth-of-type(3) h5 {
  color: #27c6b0;
  animation: gradient 6s ease infinite;
}
li:nth-of-type(3):hover h5 {
  color: #f0f0f0;
  animation: gradient 6s ease infinite;
}

li:nth-of-type(4):hover span {
  background-color: #6441a5;
  background-image: linear-gradient(270deg, #27c6b0, #6441a5);
  background-size: 400% 400%;
  animation: gradient 6s ease infinite alternate forwards;
}
li:nth-of-type(4):hover h5 {
  color: #d6249f;
}

@keyframes gradient {
  0%{background-position:0% 50%}
  50%{background-position:100% 50%}
  100%{background-position:0% 50%}
}

</style>
