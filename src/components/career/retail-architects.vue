<template>
  <div class="career">
    <img src="../../assets/retail.svg">
    <div class="details">
      <p class="title">Software Developer (Intern)</p>
      <p class="dates">July 2018 to February 2019</p>
      <p><b>Daily tools:</b>
        Python, Vue, Pentaho, PostgreSQL
      </p>
      <p class="description">
        Retail Architects was the beginning of my professional career in the 
        software industry; and it was an amazing experience being able to start
        with a small company of about 20 employees where I had the opportunity
        to really get involved in software development. As an intern, I was in
        tasked to implement an automated tagging system that would periodically
        checked the database for any new pricing or information and generate
        price tags for our customers. This allowed our customers to focus more
        on selling their products and less on keeping their inventory up to date.
      </p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import './stylesheet';

img {
  background-color: white;
  height: 175px;
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
