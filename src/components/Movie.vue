<template>
  <div class="movie">
    <div class="art">
      <img src="../assets/logo.png">
    </div>
    <div class="controls">
      <svgicon icon="heart" color="#04AC44"></svgicon>
      <button>Skip</button>
      <svgicon icon="cancel-circle" color="#04AC44"></svgicon>
    </div>
  </div>
</template>

<script>
import '../compiled-icons/heart'
import '../compiled-icons/cancel-circle'
export default {
  name: 'movie'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
