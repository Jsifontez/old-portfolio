<template>
  <div id="app">
    <mp-header></mp-header>

    <b-container>

      <mp-about></mp-about>

      <mp-skills></mp-skills>

      <mp-projects :projects='projects' id="projects"></mp-projects>

      <mp-blog></mp-blog>

      <mp-footer></mp-footer>
    </b-container>
  </div>
</template>

<script>
  import MpHeader from '@/components/layout/Header'
  import MpFooter from '@/components/layout/Footer'
  import MpAbout from '@/components/About'
  import MpProjects from '@/components/Projects'
  import MpSkills from '@/components/Skills'
  import MpBlog from '@/components/Blog'

  export default {
    name: 'app',

    components: { MpHeader, MpFooter, MpAbout, MpProjects, MpSkills, MpBlog },

    data () {
      return {
        projects: [
          {
            title: 'Platzigram',
            description: 'Este es un proyecto de platzi'
          },
          {
            title: 'Platzimusic',
            description: 'Este es un proyecto de platzi'
          },
          {
            title: 'Platzivideo',
            description: 'Este es un proyecto de platzi'
          },
          {
            title: 'Task Board',
            description: 'Este es un proyecto personal'
          }
        ]
      }
    }
  }
</script>

<style lang="scss">
  .nav-tabs{
    border: 0;
  }
  #header{
    padding: 40px 32px
  }
  #name {
    font-size: 30px;
    line-height: .5
  }
  .text{
    margin-bottom: 35px;
  }
</style>
