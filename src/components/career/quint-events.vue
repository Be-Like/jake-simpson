<template>
  <div class="career">
    <div class="image-container">
      <img src="../../assets/quintevents.png">
    </div>
    <div class="details">
      <p class="title">Junior Software Developer</p>
      <p class="dates">December 2019 to Present</p>
      <p><b>Daily tools:</b>
        Vue, Ruby on Rails, Docker, Kubernetes, AWS, PostgreSQL
      </p>
      <p class="description">
        QuintEvents has been an amazing experience. Working along side a small
        team of 5 developers has given me an opportunity to gain experience in
        just about every of the development cycle. From working with the 
        marketing team in planning and designing to building, testing and
        deploying in an agile manner. Being on a small team, it is impossible
        to hide and essential to collaborate and contribute wherever is needed.
        The opportunity and experience has been invaluable.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import './stylesheet';

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
  text-align: right;

  @media(max-width: 1000px) {
    text-align: left;
  }
}
</style>
