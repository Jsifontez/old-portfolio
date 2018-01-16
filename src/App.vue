<template>
  <b-container id="app">
    <pf-header></pf-header>

    <pf-about></pf-about>

      <pf-projects :projects='projects' id="projects">
      </pf-projects>

    <pf-footer></pf-footer>
  </b-container>
</template>

<script>
  import PfHeader from '@/components/layout/Header'
  import PfFooter from '@/components/layout/Footer'
  import PfAbout from '@/components/About'
  import PfProjects from '@/components/Projects'

  export default {
    name: 'app',

    components: { PfHeader, PfFooter, PfAbout, PfProjects },

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
    padding: 40px 0
  }
  #name {
    font-size: 30px;
    line-height: .5
  }
</style>
