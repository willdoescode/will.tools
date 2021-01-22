<template>
  <main>
    <div v-if="!onMobile">
      <a target="_blank" href="https://github.com/willdoescode" class="gh">
        <img @click="clicked" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn4.iconfinder.com%2Fdata%2Ficons%2Ficonsimple-logotypes%2F512%2Fgithub-512.png&f=1&nofb=1" alt="gh icon">
      </a>
      <div class="desktop">
          <div class="name">
            <h1>William Lane</h1>
            <GeneralAbout class="about" v-bind:is-mobile="onMobile" />
          </div>
      </div>
      <div class="text">
        <div class="t">
          <h1 class="projects-header">My projects</h1>
          <div class="projects">
              <ProjectCard
                name="Natls"
                description="The ls replacement you never knew you needed"
                img_url="https://github.com/willdoescode/nat/raw/main/assets/natbanner.png"
                project_link="https://github.com/willdoescode/nat"
              />

            <ProjectCard
              name="Wills Auto Clicker"
              description="The Fastest Java Autoclicker"
              img_url="https://github.com/willdoescode/willsautoclick/raw/master/readmeicons/dontevenask.png?raw=true"
              project_link="https://github.com/willdoescode/willsautoclick"
            />

            <ProjectCard
              name="Link Shortener"
              description="A fast link shortener"
              img_url="https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fmoorestown-mall.com%2Fnoimage.gif&f=1&nofb=1"
              project_link="https://github.com/willdoescode/linkshortener"
            />

            <ProjectCard
              name="Dotfiles"
              description="All of my dotfiles"
              img_url="https://github.com/willdoescode/dotfiles/raw/main/ss.png"
              project_link="https://github.com/willdoescode/dotfiles"
            />
          </div>
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
import ProjectCard from "@/components/ProjectCard";

export default {
  name: 'Home',
  data() {
    return {
      onMobile: this.isMobile()
    }
  },
  components: {
    GeneralAbout,
    ProjectCard
  },
  methods: {
    isMobile() {
      return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent);
    }
  }
}
</script>

<style lang="sass" scoped>
.gh
  position: absolute
  top: 3vh
  right: 3vw
  img
    width: 5vw

.desktop
  height: 100vh
  position: relative
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

.projects-header
  font-size: 2em
  text-align: center

.projects
  display: flex
  flex-direction: column
  align-items: center
</style>
