<template>
  <div class="container">
    <div>
      <h1 class="title">
        Couch to 5k
      </h1>

      <Intro/>
    </div>
  </div>
</template>

<script>
import Intro from '~/components/Intro.vue'

export default {
  components: {
    Intro
  }
}
</script>

<style scoped>
.container {
  margin: 0 auto;
  max-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;

  padding-top: 2%;
  padding-bottom: 5%;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
