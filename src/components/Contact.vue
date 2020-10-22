<template>
  <div id="Contact">
    <p class="header">Check Out What I'm Up To</p>
    <div class="links">
      <a href="https://github.com/Be-Like" target="_blank">
        <img class="github" src="../assets/GitHub_Logo_White.png">
      </a>
      <a href="https://linkedin.com/in/be-like" target="_blank" rel="noopener noreferrer">
        <img class="linkedin" src="../assets/LI-Logo.png">
      </a>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
#Contact {
  position: relative;
  height: 20vh;
  width: 100%;
  background-image: url('../assets/contact.png');
}

.header {
  color: white;
  font-family: 'Steiner';
  font-size: 25px;
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
  top: 30%;
  width: 30%;
}

.github {
  height: 25px;
}

.linkedin {
  height: 25px;
}
</style>
