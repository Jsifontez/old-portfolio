<template lang="html">
  <b-row >
    <b-col class="text-center text" sm="12">
      <h2>Proyectos</h2>
    </b-col>

    <b-col sm="12" md="4" lg="3"
      v-for="(p,i) in projects"
      :key="p.i"
    >
      <h4> {{ p.title }}</h4>
      <p>{{ p.description }}</p>
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
