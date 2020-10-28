<template>
  <div class="project-card">
    <div class="image-header">
      <img src="../../assets/stock-watcher.png" class="image">
    </div>
    <p class="body">
      My Stock Watcher is a chrome browser extension that allows users to
      create a portfolio and track the stocks they are interested in following.
      The goal in creating this extension was to simplify the process of 
      checking the stocks I owned, while also eliminating constant bombardment
      of notifications I was receiving. This extension allows the user to get
      a brief overview at the click of a button.
    </p>
    <div class="list-item">
      <img src="../../assets/creator.svg" class="icon">
      <p>Creator: Jake Simpson</p>
    </div>
    <div class="list-item">
      <img src="../../assets/github-brands-black.svg" class="icon">
      <p>Repo:
        <a href="https://github.com/Be-Like/my-stock-watcher" target="_blank">
          My Stock Watcher
        </a>
      </p>
    </div>
    <div class="list-item">
      <img src="../../assets/contribution.svg" class="icon">
      <p>Last Contribution: June 2020</p>
    </div>
    <div class="list-item">
      <img src="../../assets/coding.svg" class="icon">
      <p>Vue, Tradier API, Chrome Extension</p>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import './stylesheet.scss';
</style>
