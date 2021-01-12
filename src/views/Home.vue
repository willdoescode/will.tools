<template>
  <main>
    <div v-if="!onMobile">
      <div class="desktop">
        <h1>William Lane</h1>
        <GeneralAbout v-bind:is-mobile="onMobile" />
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
  text-align: center
</style>
