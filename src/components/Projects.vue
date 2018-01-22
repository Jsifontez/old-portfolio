<template lang="html">
  <b-row >
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
  props: {
    projects: Array
  }
}
</script>

<style lang="scss" scoped>
  .subtitle{
    margin-bottom: 0 !important
  }
</style>
