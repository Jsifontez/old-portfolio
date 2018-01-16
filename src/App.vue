<template>
  <b-container id="app">
    <pf-header></pf-header>

    <pf-about></pf-about>

    <pf-footer></pf-footer>
  </b-container>
</template>

<script>
  import PfHeader from '@/components/layout/Header'
  import PfFooter from '@/components/layout/Footer'
  import PfAbout from '@/components/About'

  export default {
    name: 'app',

    components: { PfHeader, PfFooter, PfAbout },

    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
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
