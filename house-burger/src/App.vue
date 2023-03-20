<template>
  <Header />
  <Landing />
  <Page1 />
  <Page2 />
  <Page3 />
  <Page4 />
  <Page5 />
</template>

<script>
import Header from './components/Header.vue'
import Landing from './components/Landing.vue'
import Page1 from './components/Page1.vue'
import Page2 from './components/Page2.vue'
import Page3 from './components/Page3.vue'
import Page4 from './components/Page4.vue'
import Page5 from './components/Page5.vue'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap/dist/js/bootstrap.js'
import '@fortawesome/fontawesome-free/css/all.css'


export default {
  name: 'App',
  components: {
    Header,
    Landing,
    Page1,
    Page2,
    Page3,
    Page4,
    Page5,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
