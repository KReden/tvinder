<template>
  <div class="movies">
    <div class="movie-poster-container">
      <img class="movie-poster" v-bind:src="extractImageUrl">
      <div class="movie-name">  {{ extractImageName }} </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'movies',

  props: {
    image: {
      type: Object,
      required: true
    }
  },

  computed: {

    extractImageUrl() {
      const self = this

      return self.image.url
    },

    extractImageName() {
      const self = this

      return self.image.name
    }

  },


}

</script>

<style>
.movie-poster-container {
  width: 30em;
  object-fit: cover;
  margin: 0 auto;
}
.movie-poster {
  height: 30em;
}
</style>
