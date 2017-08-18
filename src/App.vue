<template>
  <div id="app">
    <div class="nav has-shadow">
      <div class="container">
        <div class="nav-left">
          <a class="nav-item" href="/">{{ company }}</a>
        </div>
  
        <span class="navbar-burger" v-on:click="toggleNav" v-bind:class="{'is-active': isActive}">
          <span></span>
          <span></span>
          <span></span>
        </span>
  
        <div class="nav-right nav-menu" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
  
          <router-link to="/" class="nav-item r-item">Home</router-link>
          <router-link to="about" class="nav-item r-item">About</router-link>
          <router-link to="contact" class="nav-item r-item">Contact me</router-link>
          <router-link to="faq" class="nav-item r-item">FAQ</router-link>
  
          <div class="nav-item">
            <p class="control">
              <a class="button is-primary is-outlined" href="https://github.com/JosuJubera/vue-proyecto">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Get the code</span>
              </a>
            </p>
          </div>
  
        </div>
      </div>
    </div>
  
    <router-view></router-view>
  
    <footer class="footer is primary">
      <div class="container">
        <div class="content has-text-centered">
          <p>
            You can find the code on github.com
            <a class="icon" href="https://github.com/JosuJubera/vue-proyecto">
              <i class="fa fa-github"></i>
            </a>
          </p>
          <p>
            {{ year }}
          </p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      isActive: false,
      company: 'Vue project',
      year: new Date().getFullYear() + ' - Vue-project'
    }
  },
  methods: {
    toggleNav: function () {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq.sass'

.nav
  background-color: #383838

.nav-item a:not(.button):hover, a.nav-item:not(.button):hover
  color: gray

.nav-left a:not(.button), a.nav-left:not(.button)
  color: #FFF
  font-weight: bold

a.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem
  +mobile
    color: gray
    &:hover
      background-color: #F1F1F1

.navbar-burger span
  background-color: #C1C1C1

.footer
  background-color: $primary !important
  color: #FFF
  .icon
    color: #FFF
    //margin-left: 20px
</style>
