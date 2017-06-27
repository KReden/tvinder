<template>
  <div class="movies">
    <div class="movie-poster-container">
      <div class="transition-container">
        <transition name="fade">
          <img class="movie-poster" v-bind:src="extractImageUrl" v-bind:key="extractImageUrl">
        </transition>
      </div>
      <div class="movie-name">{{ extractImageName }}</div>
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
  padding: .5em 0 1em 0;
  width: 30em;
  object-fit: cover;
  margin: 0 auto;
}

.transition-container, .movie-poster {
  height: 30em;
}

.movie-poster {
  position: absolute;
  left: 0;
  right: 0;
  margin: 0 auto;
}

.movie-name {
  padding: .5em;
  font-size: 1.25em;
}


.fade-enter-active {
  transition: all .8s ease;
}
.fade-leave-active {
  transition: all .3s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
.fade-leave-to {
  transform: translateY(-100px);
}

</style>
