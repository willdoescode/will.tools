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
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus accusantium, aliquam aliquid autem, cupiditate distinctio dolorem doloremque esse eveniet ex explicabo illum iure libero maiores natus necessitatibus neque nisi nobis quasi quia quibusdam quidem quisquam, sed velit voluptates. A accusamus aliquam beatae eius enim et facilis harum, labore necessitatibus nisi odio placeat recusandae, repudiandae soluta temporibus totam ullam! Corporis itaque non nostrum soluta veritatis. Cum nobis optio possimus quia quis. Dicta minus non pariatur possimus quae quaerat velit veniam. Animi consequuntur corporis culpa cupiditate debitis dolor earum enim ex illo, ipsum labore magni necessitatibus qui repellat, rerum sequi similique vitae voluptas! A amet atque dicta dolor dolorem, doloremque ea, eligendi, enim eos exercitationem ipsum iusto magnam modi nulla obcaecati optio possimus rem. Asperiores debitis dolor ea, esse excepturi expedita facere facilis ipsam laborum laudantium nemo nobis obcaecati placeat quae quas quia saepe sed similique soluta tenetur? Cupiditate delectus deleniti esse impedit rerum! Ad aliquam consectetur cumque dicta dignissimos eaque eius enim facere inventore ipsam, iure laboriosam magni nemo nesciunt nulla provident quibusdam veniam voluptatibus. A aliquam cupiditate eius eligendi id impedit, ipsum itaque libero magnam, minus modi nemo officia porro recusandae repellat saepe velit voluptates. Cum, dignissimos enim et eveniet exercitationem iste, modi nostrum nulla optio praesentium quibusdam rem, repellendus reprehenderit totam vero? Aspernatur cum, dolores dolorum ea est eveniet explicabo facere harum magnam necessitatibus omnis qui, sapiente sunt. Animi iusto mollitia odit? Aliquid architecto cupiditate deserunt dolore dolorem earum et nihil odio, quod reiciendis reprehenderit temporibus voluptatum? Aut blanditiis consequuntur cupiditate dignissimos dolor dolorum eius eos facere facilis, in ipsum maiores natus necessitatibus, neque officiis omnis perferendis quo quos ratione repellendus ut velit voluptatum? Adipisci alias aliquid asperiores at beatae blanditiis delectus dolor dolorem dolores eos ex exercitationem expedita explicabo facilis fugiat id incidunt ipsa ipsam laborum laudantium nam nemo nihil nobis nostrum odit, officia perspiciatis praesentium provident quae quasi quidem repellendus saepe sint unde velit veritatis voluptatem! At atque commodi cum distinctio dolorum eius, ex illo in iste itaque laudantium maiores neque nihil nisi officiis praesentium quas quos repudiandae tempore totam. Aliquid aperiam autem, commodi consectetur doloremque fugiat laboriosam magni non, numquam perspiciatis provident quisquam ratione sint suscipit tempora! Atque facilis illo necessitatibus! Aliquam animi, asperiores, culpa dolorum earum enim esse inventore iure nisi odit perspiciatis quasi quibusdam, reiciendis rem repudiandae. Accusamus aliquid atque dolore dolores eveniet impedit labore magnam necessitatibus optio provident quae quibusdam, quidem quisquam quod ratione saepe tenetur totam unde. Ab aliquam aspernatur atque consequatur eaque eos explicabo fugit in laborum magnam magni minus molestias nam non odit omnis, pariatur quidem. Aliquid beatae, consectetur deleniti ipsa placeat quod repellendus ut! Atque distinctio dolore doloribus facilis maxime molestiae officia optio reiciendis velit voluptates? Alias, aspernatur, beatae, ea exercitationem fugiat minima nulla porro quis rem rerum sed voluptatem! Assumenda, ipsum, iste! Et facilis fuga nobis praesentium quia. Ad impedit quis quisquam! Delectus doloremque ipsa nostrum unde voluptates. Aut dignissimos doloribus, dolorum illo inventore maxime nemo optio soluta suscipit voluptate! Dolore fugit iure laboriosam molestias obcaecati rem totam?
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
    text-align: center
.text
  width: 100vw
  display: flex
  justify-content: center
  .t
    max-width: 400px
</style>
