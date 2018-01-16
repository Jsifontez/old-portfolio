<template>
  <b-container id="app" class="bv-example-row bv-example-row-flex-cols">
    <pf-header>
    </pf-header>

    <pf-footer>
    </pf-footer>
  </b-container>
</template>

<script>
  import PfHeader from '@/components/layout/Header'
  import PfFooter from '@/components/layout/Footer'

  export default {
    name: 'app',

    components: { PfHeader, PfFooter },

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
