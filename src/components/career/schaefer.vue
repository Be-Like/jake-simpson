<template>
  <div class="career">
    <img v-if="screenWidth < 1000" src="../../assets/ssi-schaefer.svg">
    <div class="details">
      <p class="title">Software Developer</p>
      <p class="dates">February 2019 to December 2019</p>
      <p><b>Daily tools:</b>
        Java, Oracle SQL, Jenkins
      </p>
      <p class="description">
        SSI Schaefer is a very large warehousing logistics and management company.
        While there, I maintained and developed material flow systems for our 
        customers and handled the logistics for where and how materials are stored
        based on inventory and various requirements of our customers.
      </p>
    </div>
    <img v-if="screenWidth >= 1000" src="../../assets/ssi-schaefer.svg">
  </div>
</template>

<script>
export default {
  data() {
    return {
      screenWidth: window.innerWidth
    }
  },

  mounted() {
    window.addEventListener('resize', this.onResize);
  },

  methods: {
    onResize() {
      this.screenWidth = window.innerWidth
    }
  }
}
</script>

<style lang="scss" scoped>
@import './stylesheet.scss';

img {
  width: 450px;

  @media(max-width: 525px) {
    width: 350px;
  }

  @media(max-width: 400px) {
    width: 250px;
  }
}

.details {
  text-align: left;
}
</style>
