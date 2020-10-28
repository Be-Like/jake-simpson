<template>
  <div id="Learning">
    <div class="cover" />
    <p class="header">What I'm Currently Learning</p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
#Learning {
  background-image: url('../assets/learning.jpg');
  background-position: center bottom;
  background-size: cover;
  position: relative;
  min-height: 500px;
  width: 100%;
  background-color: white;
}

.cover {
  background-color: rgba($color: #000000, $alpha: 0.6);
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
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
</style>
