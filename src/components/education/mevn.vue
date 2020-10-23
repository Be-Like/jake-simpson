<template>
  <div class="education-card">
    <div class="image-header">
      <img src="../../assets/vue-logo.png" class="image">
    </div>
    <p class="body">
      Vue was the first JavaScript framework that I worked with. It's simplicity
      in design and use along with the clean structure of the code is amazing to
      me. Because of this, Vue is still my framework of choice
      in web development. <br/>Maximilian Schwarzmüller does a phenomenal job in
      introducing Vue and the various tools associated with it and web
      development.
    </p>
    <div class="list-item">
      <img class="icon" src="../../assets/certificate.svg">
      <p>Certificate: Vue - The Complete Guide (w/ Router, Vuex, Composition API)</p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/check-box.svg">
      <p>Completed: February 2019</p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/teacher.svg">
      <p>Instructor: Maximilian Schwarzmüller</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import './stylesheet.scss';

.education-card {
  box-shadow: 5px 4px 5px rgba(0, 189, 130, 0.6);
  color: rgb(0, 189, 130);
}
</style>
