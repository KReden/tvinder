<template>
  <div id="app">
    <AppHeader/>
    <Movie/>
  </div>
</template>

<script>

import Index from './components/Index'
import AppHeader from './components/AppHeader'
import Movie from './components/Movie'

export default {
  name: 'app',
  components: {
    AppHeader,
    Movie,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html, body {
  margin: 0;
  padding: 0;
}

h1 {
  margin: 0;
  padding: 0;
}
</style>
