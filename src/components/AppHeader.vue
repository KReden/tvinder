<template>
  <div class="header">
    <div class="header--left">
      <h1>tvinder</h1>
    </div>
    <div class="header--right">
      <h1>likes</h1>
      <div class="header__data">
        <h1>{{ likes }}</h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'header',

  props: {
    likes: {
      type: Number,
      required: true
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  background-color: #04AC44;
  color: #FFF;
  padding: 15px 10px;
}

.header__data {
  background-color: #FFF;
  color: #04AC44;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  margin-left: 10px;
}

.header--left {
  /*  placeholder */
}

.header--right {
  display: flex;
  align-items: center;
}

</style>
