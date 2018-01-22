<template lang="html">
  <footer id="contact" class="container-fluid">
    <b-row align-v="center">
      <b-col cols="12 text-center" class="subtitle">
        <p>
          Juan Sifontez © 2018
          <a href="mailto:juansfontz@gmail.com">
            <strong><i class="far fa-envelope fa-lg"></i></strong>
          </a>
          <a href="https://twitter.com/Jsifontz_?lang=es" target="_blank">
            <i class="fab fa-twitter fa-lg"></i>
          </a>
          <a href="https://github.com/JSifontz" target="_blank">
            <i class="fab fa-github fa-lg"></i>
          </a>
          <a href="https://www.linkedin.com/in/juan-sifontez-924761133/" target="_blank">
            <i class="fab fa-linkedin-in fa-lg"></i>
          </a>
        </p>
      </b-col>

    </b-row>
  </footer>
</template>

<style lang="scss" scoped>
  footer{
    background-color: #9fcc4e;
    min-height: 20vh;

    p{
      margin-top: 20px;
      color: black;
    }

    .subtitle a{
      color: black;
    }

    .subtitle a:hover{
      color: #ffffb0;
    }

  }
</style>
