<template>
  <main>
    <div v-if="!isMobile">
      <div class="desktop">
        <h2 class="about">Full Stack Developer</h2>
      </div>
    </div>
    <div v-else>
      <div class="mobile">
        You are on mobile
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'GeneralAbout',
  data() {
    return {
    }
  },
  methods: {
  },
  props: {
    isMobile: Boolean
  }
}
</script>

<style lang="sass" scoped>
.about
  color: #05386B
</style>
