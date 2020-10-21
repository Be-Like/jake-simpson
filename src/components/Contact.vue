<template>
  <div id="Contact">
    <p class="header">See What I'm Up To</p>
    <div class="links">
      <img class="github" src="../assets/GitHub_Logo.png">
      <img class="linkedin" src="../assets/linked-in.svg">
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
  background-color: white;
}

.header {
  margin: 0;
  padding: 0;
}

.links {
  background-color: red;
  display: flex;
  justify-content: space-between;
  width: 30%;
  margin: 40px auto;
}

.github {
  height: 25px;
}

.linkedin {
  height: 25px;
}
</style>
