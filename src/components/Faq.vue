<template>
  <div class="faq">
    <div class="container">
      <div class="section">
        <h1 class="title">FAQ</h1>
        <h2 class="subtitle">Frecuently asked questions</h2>
        <h3>(This faqs are taken from jsonplaceholder.typicode.com/posts)</h3>
  
        <div class="columns" v-if="faqs && faqs.length">
          <div class="column is-one-third" v-for="faq of faqs">
            <div class="card">
              <div class="card-content">
                <p class="title">{{ faq.title }}</p>
                <p class="answer">{{ faq.body }}</p>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'faq',
  data: () => ({
    faqs: [],
    errors: []
  }),

  created() {
    axios.get('http://jsonplaceholder.typicode.com/posts')
      .then(response => {
        this.faqs = response.data.slice(0, 9);
      })
      .catch(e => {
        this.errors.push(e);
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
@import '../mq.sass'

.pd
  padding: 2.5em 1.5em 0

.answer
  margin-top: 10px !important
  color: gray

.columns
  flex-wrap: wrap

h2
  margin: 1.5rem 0 2rem 0 !important
h3
  margin: 1.5rem 0 2rem 0 !important
</style>
