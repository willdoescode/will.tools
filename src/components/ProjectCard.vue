<template>
  <main class="card">
    <div class="name">{{name}}</div>
    <div class="description">{{description}}</div>
    <a target="_blank" :href="project_link">
      <img :src="img_url" alt="project image">
    </a>
  </main>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    name: String,
    description: String,
    img_url: String,
    project_link: String,
  }
}
</script>

<style lang="sass" scoped>
.card
  position: relative
  display: flex
  flex-direction: column
  align-items: center
  justify-content: center
  width: 20vw
  height: 40vh
  overflow: scroll
  .name
    text-align: center
    font-size: large
    font-weight: bold
    margin-bottom: 10px

  .description
    margin-bottom: 5px
  img
    width: 20vw
    height: 20vh
    bottom: 0
</style>
