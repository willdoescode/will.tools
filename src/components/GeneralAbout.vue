<template>
  <main>
    <div v-if="!isMobile">
      <div class="desktop">
        <h2 class="about">{{age}} year old Full Stack Developer</h2>
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
      age: this.getAge()
    }
  },
  methods: {
    getAge() {
      const date = new Date()
      if (date.getMonth() >= 9 && date.getDay() >= 23) {
        return date.getFullYear() - 2006
      } else {
        return date.getFullYear() - 2007
      }
    }
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
