<template>
  <div id="Career">
    <p class="header">Career</p>
    <div class="career-container">
      <QuintEvents />
      <Schaefer />
      <RetailArchitects />
    </div>
  </div>
</template>

<script>
import QuintEvents from './career/quint-events'
import Schaefer from './career/schaefer'
import RetailArchitects from './career/retail-architects'

export default {
  components: {
    QuintEvents,
    Schaefer,
    RetailArchitects
  }
}
</script>

<style lang="scss" scoped>
#Career {
  background-image: url('../assets/career-purple.jpg');
  background-position: center;
  background-size: cover;
  position: relative;
  min-height: 500px;
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

.career-container {
  padding: 60px 0 50px;
}
</style>
