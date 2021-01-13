<template>
  <main>
    <div v-if="!onMobile">
      <div class="desktop">
          <div class="name">
            <h1>William Lane</h1>
            <GeneralAbout class="about" v-bind:is-mobile="onMobile" />
          </div>
      </div>
      <div class="text">
        <div class="t">
        </div>
      </div>
    </div>
    <div v-else>
      <div class="mobile">
        <h1>You are on Mobile</h1>
        <GeneralAbout v-bind:is-mobile="onMobile" />
      </div>
    </div>
  </main>
</template>

<script>
import GeneralAbout from "@/components/GeneralAbout";

export default {
  name: 'Home',
  data() {
    return {
      onMobile: this.isMobile()
    }
  },
  components: {
    GeneralAbout
  },
  methods: {
    isMobile() {
      return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
    }
  }
}
</script>

<style lang="sass" scoped>
.desktop
  height: 100vh
  position: relative
  margin-bottom: 50vh
  width: 100vw
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center
  .name
    h1
      font-size: 10em
      font-weight: bold
      margin: 0
    text-align: center
  .about
    font-size: 1.4em

//.text
//  width: 100vw
//  display: flex
//  justify-content: center
//  .t
//    max-width: 400px
</style>
