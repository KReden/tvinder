<template>
  <div id="app">
    <AppHeader />
    <Movies :image="image" />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader'
import Movies from './components/Movies'

import movieData from './assets/movie-data.json'

export default {
  name: 'app',
  components: {
    AppHeader,
    Movies,
  },

  data() {
    return {
      imageIndex: 0,
      movieData: movieData.posters,
    }

  },

  computed: {
    image() {
      const self = this
      return self.movieData[self.imageIndex]
    }
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
