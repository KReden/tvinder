<template>
  <div class="actions">
    <div class="controls">
    <div class="icon-button" v-on:click="decrement()">
        <svgicon id="cancel" icon="cancel-circle" color="#04AC44" ></svgicon>
      </div>
      <a id="skip" href="#"  v-on:click.prevent="skip" class="icon-button">Skip</a>
    <div class="icon-button" v-on:click="increment()">
      <svgicon id="heart" icon="heart" color="#04AC44"></svgicon>
    </div>

    </div>
  </div>
</template>

<script>
import '../compiled-icons/heart'
import '../compiled-icons/cancel-circle'
export default {
  name: 'actions',

  methods: {
    skip() {
      const self = this
      self.$emit('handleSkip')
    },

    increment() {
      const self = this
      self.$emit('handleLikes', 1)
    },

    decrement() {
      const self = this
      self.$emit('handleLikes', -1)
    }  
  }
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#skip {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.25em;
  text-decoration:none;
  color: inherit;
}

#heart {
  width: 3em;
  height: 3em;
}
#cancel {
  width: 3em;
  height: 3em;
}

.icon-button {
  cursor: pointer;
  width: 5em;
  margin: 0 1em 0 1em;
}

.controls {
  display: flex;
  justify-content: center;
}
</style>
