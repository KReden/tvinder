<template>
  <div class="index">
    We are going to put our awesome vue app in this

    <movie></movie>
  </div>
</template>

<script>
import Movie from './Movie'

export default {
  name: 'index',
  components: {
    Movie
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
