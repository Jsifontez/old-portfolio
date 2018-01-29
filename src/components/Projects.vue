<template lang="html">
  <b-row id="projects">
    <b-col class="text-center subtitle" sm="12">
      <h2>Projects</h2>
    </b-col>

    <b-col
      sm="12"
      md="4"
      lg="3"
      v-for="(p,i) in projects"
      :key="p.i"
      class="projects"
    >
      <a
        :href="p.src"
        target="_blank"
      >
        <h4 class="subtitle"> {{ p.title }}</h4>
        <p class="description">{{ p.description }}</p>
      </a>
    </b-col>
  </b-row>
</template>

<script>
export default {
  data () {
    return {
      projects: [
        {
          title: 'Platzigram',
          description: 'Este es un proyecto de platzi',
          src: 'https://github.com/JSifontz/platzigram'
        },
        {
          title: 'Platzimusic',
          description: 'Este es un proyecto de platzi',
          src: 'https://platzimusic-bnnfdkylxp.now.sh/'
        },
        {
          title: 'Platzivideo',
          description: 'Este es un proyecto de platzi',
          src: 'https://jsifontz.github.io/platzi-video/'
        },
        {
          title: 'Task Board',
          description: 'Este es un proyecto personal',
          src: 'https://codepen.io/Jsifontz/full/EobZWV/'
        },
        {
          title: 'Randon Quote Machine',
          description: 'Este es un proyecto personal',
          src: 'https://codepen.io/Jsifontz/full/veBQXm/'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .subtitle{
    margin-bottom: 0 !important;
  }

  #projects{
    min-height: 53vh;
  }

  .projects>a:hover{
    text-decoration: none
  }
</style>
