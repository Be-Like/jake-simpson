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
      <img class="image" src="../../assets/u-of-sc-long-red.png" alt=""/>
    </div>
    <!-- <p class="header">University of South Carolina</p> -->
    <p class="body">
      While studying at USC, I discovered that I have a passion for learning.
      My desire for discovery and knowledge of how things work led me to seek
      scholarship in an industry that will never quench that passion.
      Technology! In an industry that is ever in motion, I am always thrilled
      to learn about and to be a part of the new and emerging tech. This is
      what led me to seek and acquire a degree in Computer Science.
    </p>
    <div class="list-item">
      <img class="icon" src="../../assets/diploma.svg">
      <p>Bachelor of Science in Computer Science</p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/mortarboard.svg">
      <p>Graduated: May 2019</p>
    </div>
    <div class="list-item">
      <img class="icon" src="../../assets/mobile-phone.svg">
      <p>Capstone: TimeKeepers (Android Native Application)</p>
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
  box-shadow: 5px 4px 5px rgba(115, 0, 10, 0.6);
  color: rgb(115, 0, 10);
}
</style>
