<template>
  <main>
    <div v-if="!isMobile">
      <div class="desktop">
        You are not on mobile
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
  props: {
    isMobile: Boolean
  }
}
</script>
