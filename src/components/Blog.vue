<template lang="html">
  <b-row class="blog">
    <b-col class="text-center text" sm="12">
      <h2>Artículos</h2>
    </b-col>

    <b-col sm="12" md="4" lg="3"
      v-for="(a,i) in articles"
      :key="a.i"
    >
      <a :href="a.src" target="_blank">
        <div class="img-container">
          <b-img :src="a.img" fluid-grow center height="305" width="205"/>
        </div>
        <p class="title"> {{ a.title }}</p>
      </a>
    </b-col>
  </b-row>
</template>

<script>
export default {
  data () {
    return {
      articles: [
        {
          img: 'https://cdn-images-1.medium.com/max/2000/1*dk348FRrIv8HigiYewhUTw.jpeg',
          title: 'Lo que debes saber para aplicar Responsive Design',
          src: 'https://medium.com/@Jsifontez/lo-que-debes-saber-para-aplicar-responsive-design-8c0fe4ae7eda'
        },
        {
          img: 'https://cdn-images-1.medium.com/max/2000/1*dk348FRrIv8HigiYewhUTw.jpeg',
          title: '¿Qué es Responsive Design?',
          src: 'https://medium.com/@Jsifontez/qu%C3%A9-es-responsive-design-3448ab0a7fe8'
        },
        {
          img: 'https://cdn-images-1.medium.com/max/800/1*SPGssQmQgoZyqNKc_UZUPQ.png',
          title: 'Aprendiendo Git y Github: Parte 3',
          src: 'https://medium.com/@Jsifontez/aprendiendo-git-y-github-parte-3-b83bd5a5b0e6'
        },
        {
          img: 'https://cdn-images-1.medium.com/max/800/1*SPGssQmQgoZyqNKc_UZUPQ.png',
          title: 'Aprendiendo Git y Github: Parte 2',
          src: 'https://medium.com/@Jsifontez/aprendiendo-git-y-github-parte-2-d8e90d27f612'
        },
        {
          img: 'https://cdn-images-1.medium.com/max/800/1*SPGssQmQgoZyqNKc_UZUPQ.png',
          title: 'Aprendiendo Git y Github: Parte 1',
          src: 'https://medium.com/@Jsifontez/aprendiendo-git-y-github-parte-1-3366297342ce'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  .blog a .title{
    text-decoration: none;
    color: grey;
  }

  a:link{
    text-decoration: none;
  }
</style>
