<template>
  <div id="app">
    <!-- TODO: header -->
    <Header />
    <!-- TODO: main -->
    <Products />
    <!-- TODO: footer -->
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Products from './components/Products.vue'

 

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Products
  }
}
</script>

<style lang="scss">
  @import "../style/generals";
  @import "../style/vars";


</style>
