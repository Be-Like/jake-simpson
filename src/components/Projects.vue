<template>
  <div id="Projects">
    <div class="cover"/>
    <p class="header">Personal Projects</p>
    <div class="projects-container">
      <Tisn />
      <StockWatcher />
      <MaintenanceMan />
    </div>
  </div>
</template>

<script>
import Tisn from './projects/tisn'
import StockWatcher from './projects/stockWatcher'
import MaintenanceMan from './projects/maintenanceMan'

export default {
  components: {
    Tisn,
    StockWatcher,
    MaintenanceMan
  }
}
</script>

<style lang="scss" scoped>
#Projects {
  background-image: url('../assets/projects.jpg');
  background-position: center;
  background-size: cover;
  min-height: 500px;
  position: relative;
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
  margin: 15px;
  padding: 0;
  position: absolute;
  right: 0;
  top: 0;
}

.projects-container {
  position: relative;
  padding-top: 60px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
</style>
