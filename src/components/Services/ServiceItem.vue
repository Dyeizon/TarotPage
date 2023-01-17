<script>
    export default {
        props: {
            title: String,
            background: String,
            destination: String
        },

        computed: {
            serviceStyle() {
                return 'background-image: url(' + this.background + ');';
            }
        }
    }
</script>
<template>
    <a :href="destination">
        <div class="service-icon" :style="serviceStyle">

        </div>
        <div class="service-desc">
            <h4>{{ title }}</h4>
        </div> 
    </a>

</template>
<style scoped>
    

    .service-icon {
        width: 250px;
        height: 250px;
        border-radius: 100%;
        background-position: center;
        background-size: 100%;
        border: 2px solid rgba(0, 0, 0, 0.5);

        transition: background-size 0.5s;
    }

    .service-desc {
        margin-top: 10px;
        text-align: center;
        color: white;
    }

    a {
        text-decoration: none;
    }

    a:hover .service-icon {
        background-size: 130%;
    }
    
</style>