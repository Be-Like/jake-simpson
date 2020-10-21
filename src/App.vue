<template>
  <div class='root'>
    <img class='background' ref='background' src='./assets/family.jpg'/>
    <!-- <img class='foreground' ref='foreground' src='./assets/tree-foreground.png'/> -->
    <div class='section section-1' ref='first'>
      <div>
        <p>Hi, I'm <br/> Jake Simpson</p>
      </div>
    </div>
    <div class='section section-2' ref='second'>
      <div>
        <h2> Here's more info </h2>
        <p> Lorem ipsum dolor, sit amet consectetur adipisicing elit...</p>
      </div>
    </div>
  <div class="section test">
    <h3>Just another test</h3>
  </div>
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'

export default {
  name: 'App',

  setup () {
    const foreground = ref(null)
    const background = ref(null)
    const first = ref(null)
    const second = ref(null)

    const handleScroll = () => {
      const scrollY = window.scrollY
      if (scrollY > 1300) return

      // decreases as user scrolls
      first.value.style.opacity = (100 - ((scrollY + window.innerHeight) - first.value.offsetHeight)) / 100
      // increases as user scrolls
      second.value.style.opacity = ((scrollY + window.innerHeight) - second.value.offsetTop) / 100

      const maxBackgroundSize = 120;
      const backgroundSize = ((scrollY) / (maxBackgroundSize - 100)) // increases as user scrolls

      // zoom the background at a slower rate
      background.value.style.transform = 'scale(' + (100 + backgroundSize * .4) / 100 + ')'
      // foreground.value.style.transform = 'scale(' + (100 + backgroundSize) / 100 + ')'
    }

    onMounted(() => {
      document.addEventListener('scroll', handleScroll)
    })

    onUnmounted(() => {
      document.removeEventListener('scroll', handleScroll)
    })

    return {
      foreground,
      background,
      first,
      second
    }
  },
}
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.test {
  width: 100%;
  background-color: aqua;
}
img.background, img.foreground {
    /* Fill background */
    min-height: 100%;
    min-width: 1024px;

    /* Scale proportionately */
    width: 100%;
    height: auto;
}
img.background {
    /* Positioning */
    position: fixed;
    margin-top: -10%;
    top: 0;
    left: 0;

    @media(max-width: 1100px) {
      margin-top: -5%;
    }
}
.section {
    min-height: 100vh;
    position: relative;
}

.section > div {
  position: fixed;
  color: white;
  right: 0;
  margin-top: 10%;
  margin-right: 10%;

  @media(max-width: 925px) {
    /* centers this div */
    left: 50%;
    top: 50%;
    transform: translate(-50%, 55%);
  }
}

.section-1 {
  margin-bottom: 500px; /* determines the gap between our two sections */
  font-size: 4em;
  text-align: right;
  @media(max-width: 925px) {
    text-align: center;
    font-size: 3em;
  }
  /* background-color: rgba(255, 255, 255, 0.7); */
}

.section-2 {
  opacity: 0; /* defaults to 0 because it's not visible */
}

.section-2 div {
  background-color: rgba(255, 255, 255, 0.7);
  color: black;
  text-align: center;
  padding: 50px;
  max-width: 300px;
}

.section-2 h2 {
  font-size: 2em;
  margin-bottom: 40px;
}

.section-2 p {
  line-height: 150%;
}
</style>
