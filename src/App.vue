<script>
import Header from './components/Header/Header.vue';
import Carousel from './components/Carousel/Carousel.vue';
import Services from './components/Services/Services.vue';
import Footer from './components/Footer/Footer.vue';

  export default {
    components: {
      Header,
      Carousel,
      Services,
      Footer
    }
  }
</script>

<template>
  <Header></Header>
  <Carousel></Carousel>
  <Services></Services>
  <Footer></Footer>
</template>

<style scoped>
</style>
