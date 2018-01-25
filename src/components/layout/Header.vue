<template lang="html">
  <header id="header" class="subtitle">
    <b-navbar toggleable="md">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>

      <b-navbar-brand href="#about" @click="changeToAbout">Juan Sifontez</b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">

        <b-navbar-nav class="sections">
          <b-nav-item href="#projects" @click="changeToProjects">Proyectos</b-nav-item>
          <b-nav-item href="#blog" @click="changeToBlog">Blog</b-nav-item>
          <b-nav-item href="#contact">Contacto</b-nav-item>
        </b-navbar-nav>

        <b-navbar-nav class="ml-auto">
          <b-nav-item href="https://www.linkedin.com/in/juan-sifontez-924761133/" target="_blank">
            <i class="fab fa-linkedin-in fa-lg"></i>
          </b-nav-item>
          <b-nav-item href="https://github.com/JSifontz" target="_blank">
            <i class="fab fa-github fa-lg"></i>
          </b-nav-item>
          <b-nav-item href="https://twitter.com/Jsifontz_?lang=es" target="_blank">
            <i class="fab fa-twitter fa-lg"></i>
          </b-nav-item>
          <b-nav-item href="mailto:juansfontz@gmail.com" target="_blank">
            <i class="far fa-envelope fa-lg"></i>
          </b-nav-item>
          <b-nav-item href="https://medium.com/@Jsifontez" target="_blank">
            <i class="fab fa-medium-m fa-lg"></i>
          </b-nav-item>
          <b-nav-item href="https://www.facebook.com/juansifontez/" target="_blank">
            <i class="fab fa-facebook-f fa-lg"></i>
          </b-nav-item>
        </b-navbar-nav>

      </b-collapse>

    </b-navbar>
  </header>
</template>

<script>
  export default {
    methods: {
      changeToAbout () {
        this.$emit('changeToAbout')
      },
      changeToProjects () {
        this.$emit('changeToProjects')
      },
      changeToBlog () {
        this.$emit('changeToBlog')
      }
    }
  }
</script>

<style lang="scss" scoped>
  $primary: #9fcc4e;
  $secondary-l: #ffffb0;

  header{
    background-color: $primary;
    font-weight: bold;
    padding: 40px 32px;

    #nav_collapse a:hover{
      color: $secondary-l;
    }


  }
</style>
