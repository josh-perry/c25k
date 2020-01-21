<template>
  <div>
    <Navbar/>

    <div class="container">
      <nuxt />
    </div>

    <Footer/>
  </div>
</template>

<script scoped>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style scope>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

.container {
  margin: 0 auto;
  padding-top: 2%;
  padding-bottom: 5%;
}

p {
  text-align: left;
}
</style>
