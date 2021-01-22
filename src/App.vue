<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="sass">
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap')
body
  font-family: 'Ubuntu', sans-serif
  color: #EDF5E1
  background-color: #5CDB95
  height: 100vh
  transition: 1.5s
</style>

<script>
export default {
  name: 'App',
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      console.log(window.pageYOffset)
      if (window.pageYOffset > window.innerHeight / 4) {
        document.body.style = 'background-color: #379683'
      } else {
        document.body.style = 'background-color: #5CDB95'
      }
    }
  },
}
</script>
