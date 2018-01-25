<template>
  <div id="app">
    <mp-header v-on:changeActive="toogleActive"></mp-header>

    <b-container>

      <mp-about :active="active"></mp-about>

      <mp-skills></mp-skills>

      <mp-projects :projects='projects' id="projects"></mp-projects>

      <mp-blog></mp-blog>

    </b-container>
    <mp-footer></mp-footer>
  </div>
</template>

<script>
  import MpHeader from '@/components/layout/Header'
  import MpFooter from '@/components/layout/Footer'
  import MpAbout from '@/components/About'
  import MpProjects from '@/components/Projects'
  import MpSkills from '@/components/Skills'
  import MpBlog from '@/components/Blog'

  window.addEventListener('scroll', function (e) {
    // console.log(window.scrollY)

    if (window.scrollY >= 240 && window.scrollY <= 279) {
      console.log('YA ESTAMOS AQUI')
    }
  })

  export default {
    name: 'app',

    components: { MpHeader, MpFooter, MpAbout, MpProjects, MpSkills, MpBlog },

    data () {
      return {
        active: {
          about: false,
          projects: false,
          blog: false
        },
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
    },
    methods: {
      toogleActive () {
        this.active.about = true
        this.active.project = false
        this.active.blog = false
      }
    }
  }
</script>

<style lang="scss">
  #app{
    background-color: #fffff2;
  }

  .subtitle{
    font-weight: bold;
    margin-bottom: 35px;
    font-family: 'Varela Round', sans-serif;
    color: #9fcc4e;
  }

  .description{
    font-family: 'Montserrat', sans-serif;
    color: darkgreen;
  }

  .move-enter-active, .move-leave-active {
    transform: translateX(0);
    transition: all .3s linear;
    }

  .move-enter, .move-leave-to {
    transform: translateX(100%);
  }
</style>
