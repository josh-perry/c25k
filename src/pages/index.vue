<template>
  <div>
    <h1 class="title">
      Couch to 5k
    </h1>

    <Intro/>
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
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
  text-align: center;
}
</style>
