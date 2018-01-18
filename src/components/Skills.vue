<template lang="html">
  <b-row id="skills">
    <b-col sm="12" class="text-center text">
      <h3>Habilidades</h3>
    </b-col>
    <b-col cols="3"
      v-for="l in logos"
      :key="l.id"
      class="skills-images"
    >
      <b-img-lazy
        :src='l.src'
        fluid :alt="l.id"
        height="100"
        width="100"
        blank-color="#bbb"
        center
      />
    </b-col>
  </b-row>
</template>

<script>
  import html from '@/assets/HTML_logo.png'
  import css from '@/assets/css_logo.png'
  import js from '@/assets/javascript_logo.png'
  import react from '@/assets/react_logo.png'
  import vue from '@/assets/vue_logo.png'
  import webpack from '@/assets/webpack_logo.png'
  import git from '@/assets/git_logo.png'
  import bootstrap from '@/assets/bootstrap_logo.png'

  export default {
    data () {
      return {
        logos: [
          { id: 'html', src: html },
          { id: 'css', src: css },
          { id: 'javascript', src: js },
          { id: 'vue', src: vue },
          { id: 'react', src: react },
          { id: 'git', src: git },
          { id: 'webpack', src: webpack },
          { id: 'bootstrap', src: bootstrap }
        ]
      }
    }
  }
</script>

<style lang="scss"  scoped>
  #skills{
    margin: 35px 0;
  }

  .skills-images{
    margin-bottom: 20px;
  }
</style>
