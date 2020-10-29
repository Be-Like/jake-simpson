<template>
  <div class='root'>
    <img
      v-if="screenWidth >= 575"
      class='background'
      ref='background'
      src='./assets/family.jpg'
    />
    <img
      v-if="screenWidth < 575"
      class='background'
      ref='background'
      src='./assets/family-mobile.jpg'
    />
    <div class="foreground" />
    <div class='section section-1' ref='first'>
      <div>
        <p>Hi, I'm <br/> Jake Simpson</p>
      </div>
    </div>
    <div class='section section-2' ref='second'>
      <div>
        <p>A software engineer and family man</p>
      </div>
    </div>
    <Learning />
    <Projects />
    <Career />
    <Education />
    <Contact />
  </div>
</template>

<script>
import Learning from './components/Learning'
import Projects from './components/Projects'
import Career from './components/Career'
import Education from './components/Education'
import Contact from './components/Contact'
import { ref, onMounted, onUnmounted } from 'vue'

export default {
  name: 'App',

  components: {
    Learning,
    Projects,
    Career,
    Education,
    Contact
  },

  data() {
    return {
      screenWidth: window.innerWidth
    }
  },

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

  mounted() {
    window.addEventListener('resize', this.onResize);
  },

  methods: {
    onResize() {
      this.screenWidth = window.innerWidth
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: 'Steiner';
  src: local('Steiner'), url('./assets/fonts/Steinerlight.ttf') format('truetype');
}
@font-face {
  font-family: 'Electro';
  src: local('Electro'), url('./assets/fonts/Electrolize-Regular.ttf') format('truetype');
}
body {
  margin: 0;
  padding: 0;
}
#app {
  color: #2c3e50;
  background-color: black;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>

<style lang="scss" scoped>
img.background, div.foreground {
    /* Fill background */
    min-height: 100%;
    min-width: 1024px;

    @media(max-width: 575px) {
      min-width: 505px;
    }

    /* Scale proportionately */
    width: 100%;
    height: auto;
}
img.background {
    /* Positioning */
    position: fixed;
    top: 0;
    left: 0;

    @media(min-width: 1300px) {
      margin-top: -5%;
    }
    @media(max-width: 575px) {
      margin-top: 0;
    }
    @media(max-width: 505px) {
      left: calc(100vw - 505px);
    }
    @media(max-width: 425px) {
      left: -80px;
    }
}
div.foreground {
  background-color: rgba($color: #000000, $alpha: 0.3);
  position: fixed;
}
.section {
    min-height: 100vh;
    position: relative;
}

.section > div {
  position: fixed;
  color: white;
}

.section-1 > div {
  right: 0;
  margin-top: 4%;
  margin-right: 8%;

  @media(max-width: 1000px) {
    left: 0;
    bottom: 0;
    margin: 0 auto;
  }
}

.section-2 > div {
  bottom: 3%;
  left: 50%;
  transform: translateX(-50%);
}

.section-1 {
  margin-bottom: 500px; /* determines the gap between our two sections */
  font-size: 4em;
  text-align: right;

  @media(max-width: 1000px) {
    text-align: center;
  }
  @media(max-width: 925px) {
    font-size: 3em;
  }
}

.section-2 {
  opacity: 0; /* defaults to 0 because it's not visible */
  font-size: 3em;
  text-align: center;
}
</style>
