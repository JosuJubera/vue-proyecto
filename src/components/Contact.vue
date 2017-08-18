<template>
  <div class="contact">
    <div class="container">
      <section class="section">
        <h1 class="title">{{ title }}</h1>
        <h2 class="subtitle">{{ subtitle }}</h2>
      </section>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'Contact',
      subtitle: 'Information not available'
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<<style lang="sass" scoped>
h2
  margin: 1.5rem 0 2rem 0 !important
</style>
