<template>
  <div id="Education">
    <p class="header">Education & Certificates</p>
    <div class="education-container">
      <usc />
      <mevn />
      <mern />
    </div>
  </div>
</template>

<script>
import usc from './education/usc'
import mevn from './education/mevn'
import mern from './education/mern'

export default {
  components: {
    usc,
    mevn,
    mern
  }
}
</script>

<style lang="scss" scoped>
#Education {
  background-image: url('../assets/education.jpg');
  background-position: left bottom;
  background-size: cover;
  min-height: 300px;
  position: relative;
  width: 100%;
}

.header {
  color: black;
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

.education-container {
  padding-top: 60px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
