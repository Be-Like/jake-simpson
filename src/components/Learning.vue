<template>
  <div id="Learning">
    <div class="cover" />
    <p class="header">What I'm Currently Learning</p>
    <div class="learning-container">
      <Overview />
      <Flutter />
    </div>
  </div>
</template>

<script>
import Overview from './learning/overview'
import Flutter from './learning/flutter'

export default {
  components: {
    Overview,
    Flutter
  }
}
</script>

<style lang="scss" scoped>
#Learning {
  background-image: url('../assets/learning.jpg');
  background-position: center bottom;
  background-size: cover;
  padding-bottom: 50px;
  position: relative;
  min-height: 500px;
  text-align: left;
  width: 100%;
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
  padding: 0;
  position: absolute;
  right: 0;
  text-align: center;
  top: 0;
}

.learning-container {
  padding-top: 60px;
  padding-right: 43%;
  position: relative;

  @media(max-width: 1000px) {
    padding-right: 0;
  }
  @media(max-width: 400px) {
    padding-top: 90px;
  }
}
</style>
