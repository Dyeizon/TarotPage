<script>    
import CarouselItem from './CarouselItem.vue';

  export default {
    components: {
      CarouselItem
    }
  }
</script>

<template>
<section>
    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="true">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <CarouselItem class="active" title="Receba aconselhamento" subtitle="Realize uma consulta com um dos nossos tarólogos" buttonText="Quero uma consulta"/>
    <CarouselItem title="Estude Tarologia" subtitle="Mais de 10 métodos de tiragem exclusivos para você" buttonText="Quero aprender"/>
    <CarouselItem title="Visite a lojinha" subtitle="Diversos itens para sua ascenção no Tarot" buttonText="Quero comprar"/>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
            
</section>
</template>

<style scoped>
.carousel, .carousel-inner{
    height: calc(100vh - 100px);
    background-color: black;
}

.carousel-item {
    height: 100%;
    width: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.carousel-item:nth-child(1) {
    background-image: url("../../assets/img/carousel-1.png");
    background-position-y: center;
}

.carousel-item:nth-child(2) {
    background-image: url("../../assets/img/carousel-2.jpg");
    background-position-y: bottom;
}

.carousel-item:nth-child(3) {
    background-image: url("../../assets/img/carousel-3.png");
    background-position-y: center;
}


</style>