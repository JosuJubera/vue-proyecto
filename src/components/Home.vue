<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-4">{{ subHeading }}</h2>
          </div>
          <a class="button is-large is-primary" id="learn" href="https://www.udemy.com/react-vs-angular-vs-vuejs-by-example/learn/v4/overview">Learn more</a>
        </div>
      </div>
    </section>
  
    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1 has-text-centered">
            <i class="fa fa-cog is-primary"></i>
          </div>
          <div class="column is-one-third-desktop">
            <p class="title">
              <strong>{{ tituloCuerpo }}</strong>
            </p>
          </div>
          <div class="column">
            <p>{{ cuerpo }}</p>
          </div>
        </div>
      </div>
  
      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Vue.js</p>
              <p class="subtitle">The Progressive JavaScript Framework.</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title">Bulma</p>
              <p class="subtitle">A modern CSS framework based on Flexbox.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data() {
    return {
      heading: 'Awesome vuejs web page',
      subHeading: 'This is a website made by vuejs framework. This website was created for a udemy.com course',
      tituloCuerpo: 'Caracteristicas',
      cuerpo: 'A continuación se muestran las características principales de la web'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq.sass'

.hero
  background: url('../assets/clouds.jpg')
  background-size: cover

  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem

h2
  margin: 1.5rem 0 2rem 0 !important

.card-content .subtitle
  margin-top: 1em

.fa-cog
  font-size: 40px

#learn
  +desktop
    margin-bottom: 2rem

.pd
  +tablet
    padding: 2em 0  

</style>
