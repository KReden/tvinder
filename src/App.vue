<template>
  <div id="app">
    <AppHeader :likes="enforcePositiveLikes"/>
    <Movies :image="image"/>
    <Actions @handleLikes="handleLikes" @handleSkip="handleSkip"/>
  </div>
</template>

<script>

import Index from './components/Index'
import AppHeader from './components/AppHeader'
import Actions from './components/Actions'
import Movies from './components/Movies'

import movieData from './assets/movie-data.json'

export default {
  name: 'app',
  components: {
    AppHeader,
    Actions,
    Movies,
  },

  data() {
    return {
      likes: 0,
      imageIndex: 0,
      movieData: movieData.posters
    }
  },

  computed: {
    enforcePositiveLikes() {
      const self = this
      if (self.likes < 0) {self.likes = 0}
      return self.likes
    },

    image() {
      const self = this
      return self.movieData[self.imageIndex]
    }
  },

  methods: {
    handleLikes(vote) {
      const self = this
      self.likes += vote
      self.incrementImage()
    },

    handleSkip() {
      const self = this
      self.incrementImage()
    },

    incrementImage() {
      const self = this

      self.imageIndex += 1

      if(self.imageIndex > (self.movieData.length-1)) {
        self.imageIndex = 0
      }
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
