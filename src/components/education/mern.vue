<template>
  <div class="education-card" :style="colorBlind ? 'color: black' : null">
    <div class="color">
      <span @click="colorBlind = !colorBlind">
        <img 
          v-if="colorBlind"
          src="../../assets/view.svg"
        />
        <img 
          v-else
          src="../../assets/invisible.svg"
        >
      </span>
    </div>
    <div class="image-header">
      <img src="../../assets/react-logo.png" class="image">
    </div>
    <p class="body">
      While not as fun to work with, and much more bloated than Vue,
      React has a very large presence in the web application development
      world. As such, I took it upon myself to get educated in working
      with React.<br/>Brad Traversy does a very good job introducing and
      expounding on React, as well as educating students in Redux.
    </p>
    <div class="list-item">
      <img class="icon" src="../../assets/certificate.svg">
      <p>
        Certificate: MERN Stack Front to Back: Full Stack React, Redux & Node.js
      </p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/check-box.svg">
      <p>Completed: October 2019</p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/teacher.svg">
      <p>Instructor: Brad Traversy</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      colorBlind: false
    }
  },
}
</script>

<style lang="scss" scoped>
@import './stylesheet.scss';

.education-card {
  box-shadow: 5px 4px 5px rgba(97, 218, 251, 0.6);
  color: rgb(97, 218, 251);
}
</style>
