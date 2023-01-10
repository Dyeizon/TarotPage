<script>
import Header from './components/Header/Header.vue';
import Carousel from './components/Carousel/Carousel.vue';

  export default {
    data() {
      return {
        count: 0
      }
    },

    methods: {
      increment() {
        this.count++;
      }
    },
    
    components: {
      Header,
      Carousel
    }
  }
</script>

<template>
  <Header></Header>
  <Carousel></Carousel>
  <h1>teste 2</h1>
</template>

<style scoped>
</style>
