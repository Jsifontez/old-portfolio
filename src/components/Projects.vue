<template lang="html">
  <b-row id="projects">
    <b-col class="text-center subtitle" sm="12">
      <h2>Proyectos</h2>
    </b-col>

    <b-col sm="12" md="4" lg="3"
      v-for="(p,i) in projects"
      :key="p.i"
    >
      <h4 class="subtitle"> {{ p.title }}</h4>
      <p class="description">{{ p.description }}</p>
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

<style lang="scss" scoped>
  .subtitle{
    margin-bottom: 0 !important;
  },
  #projects{
    min-height: 53vh;
  }
</style>
