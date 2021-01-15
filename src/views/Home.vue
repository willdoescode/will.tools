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
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Distinctio error, fuga nisi nulla odit quasi quos recusandae sit ullam! Corporis deserunt earum officia possimus quos recusandae tempora. Adipisci asperiores aut autem consequatur, debitis error fuga illum impedit laboriosam magnam modi nisi officia placeat quasi, recusandae rem saepe similique, tempora vel voluptatum? Eius provident quia quisquam recusandae sit! Aliquid delectus earum in iure maxime nam neque recusandae sit sunt ut. Ab asperiores assumenda at consectetur deserunt dolores est, harum itaque laborum, molestias nemo, odit officia recusandae reiciendis tenetur voluptatem voluptates. A ab adipisci consectetur, cupiditate doloremque eos explicabo fuga inventore ipsam laudantium mollitia nesciunt provident quo sequi, tempora tempore, velit veniam voluptatem! Consequatur corporis dolorem ea eaque eius error ex excepturi fugit id minima mollitia, pariatur praesentium quis quisquam sapiente similique unde veniam voluptatum. A accusamus adipisci alias architecto aut beatae delectus deleniti distinctio dolorem earum eligendi eos eum fugiat illum in ipsam magnam modi necessitatibus nostrum nulla odio perspiciatis porro praesentium qui ratione, repudiandae sit soluta suscipit veniam voluptatum! Ab aliquid aperiam architecto cupiditate deleniti doloribus dolorum ducimus earum, enim, eos facilis magni modi natus numquam obcaecati optio perferendis quia, quos sapiente soluta temporibus tenetur ut veniam voluptas voluptate! Aut?
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

.text
  width: 100vw
  display: flex
  justify-content: center
  .t
    max-width: 400px
</style>
