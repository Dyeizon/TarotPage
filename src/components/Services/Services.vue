<script>
    import ServiceItem from './ServiceItem.vue';

    export default {
        components: {
            ServiceItem
        }
    }
</script>
<template>
    <section id=services>
        <div class="container">  
            <h1>Nossos serviços</h1>
            <div class="services">
                <ServiceItem title="Meu arcano" background="src/assets/img/my-arcane.jpg" destination="my-arcane"></ServiceItem>
                <ServiceItem title="Carta do dia" background="src/assets/img/card-of-the-day.jpg" destination="cotd"></ServiceItem>
                <ServiceItem title="Leituras" background="src/assets/img/spreads.jpg" destination="spreads"></ServiceItem>
            </div>
        </div>
    </section>
</template>
<style scoped>
    section {
        height: calc(100vh - 100px);
        width: 100%;

        display: flex;
        align-items: center;

        /* background: rgb(146,0,255);
        background: linear-gradient(0deg, rgba(146,0,255,1) 0%, rgba(255,224,134,1) 120%); */

        background-image: url('../../assets/img/stars-background.jpeg');
        background-size: cover;
    }

    h1 {
        color: white;
        margin-bottom: 70px;
        text-align: center;
    }

    .services {
        display: flex;
        align-items: center;
        justify-content: space-around;
    }


</style>