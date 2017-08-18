<template>
  <div class="about">
    <div class="container">
      <section class="section">
        <h1 class="title">{{ title }}</h1>
        <h2 class="subtitle">{{ subtitle }}</h2>

        <p>
          This website is made by vuejs framework. It is based on 
          a course of udemy.com. Also, it uses bulma for the css.
        </p>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'About',
      subtitle: "Application's description page"
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<<style lang="sass" scoped>
h2
  margin: 1.5rem 0 2rem 0 !important
</style>
