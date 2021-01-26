<template>
  <main>
    <div v-if="!isMobile">
      <div class="desktop">
        <h2 ref="about" class="about">Full Stack Developer</h2>
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
import { TimelineLite } from 'gsap';

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
  },
  mounted() {
    const timeline = new TimelineLite();
    const {about} = this.$refs;
    timeline.fromTo(about, {opacity: 0, y: '100%'}, {x: '0', y: '0', opacity: 1, delay: 1, duration: 1})
  }
}
</script>

<style lang="sass" scoped>
.about
  color: #05386B
</style>
