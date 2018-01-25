<template>
  <div id="app">
    <mp-header
      @changeToAbout="about"
      @changeToProjects="projectsComp"
      @changeToBlog="blog"
    ></mp-header>

    <b-container>

      <transition name="fade" mode="out-in">
        <component :is="view"></component>
      </transition>

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

  export default {
    name: 'app',

    components: { MpHeader, MpFooter, MpAbout, MpProjects, MpSkills, MpBlog },

    data () {
      return {
        view: 'MpBlog'
      }
    },
    methods: {
      about () {
        this.view = 'MpAbout'
      },
      projectsComp () {
        this.view = 'MpProjects'
      },
      blog () {
        this.view = 'MpBlog'
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

  .fade-enter-active, .fade-leave-active {
    transition: opacity .3s ease;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
</style>
