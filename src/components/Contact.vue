<template>
  <div id="Contact">
    <p class="header">Check Out What I'm Up To</p>
    <div class="links">
      <a href="https://github.com/Be-Like" target="_blank">
        <img
          v-if="screenWidth > 730"
          class="github"
          src="../assets/github-long.png"
        >
        <img
          v-else
          class="github"
          src="../assets/github-brands.svg"
        >
      </a>
      <a href="https://linkedin.com/in/be-like" target="_blank">
        <img
          v-if="screenWidth > 730"
          class="linkedin" src="../assets/linkedin-long.svg"
        >
        <img
          v-else
          class="linkedin"
          src="../assets/linkedin-short.png"
        >
      </a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      screenWidth: window.innerWidth
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

<style lang="scss" scoped>
#Contact {
  background-image: url('../assets/contact.png');
  position: relative;
  padding-bottom: 50px;
  min-height: 100px;
  width: 100%;
}

.header {
  color: white;
  font-family: 'Steiner';
  font-size: 25px;
  font-weight: bold;
  left: 0;
  margin: 15px;
  padding: 0;
  position: absolute;
  right: 0;
  top: 0;
}

.links {
  bottom: 0;
  display: flex;
  height: fit-content;
  justify-content: space-between;
  left: 0;
  margin: auto;
  position: absolute;
  right: 0;
  top: 30px;
  width: 30%;

  @media(max-width: 1100px) {
    width: 50%;
  }

  @media(max-width: 725px) {
    width: 30%;
  }

  @media(max-width: 575px) {
    width: 60%;
  }

  @media(max-width: 400px) {
    width: 80%;
  }
  
  @media(max-width: 350px) {
    top: 60px;
  }
}

.github {
  height: 45px;
}

.linkedin {
  height: 45px;
}
</style>
