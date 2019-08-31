<template>
  <div>
    <Navbar />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Footer from '../layouts/Footer.vue'
import Navbar from '../layouts/Navbar.vue'
export default {
  components:{
    Footer,
    Navbar
  }
}
</script>

<style>


</style>
