<script>
    export default {
        props: {
            title: String,
            subtitle: String,
            buttonText: String
        }
    }
</script>

<template>
    <div class="carousel-item">
        <div class="organizer">
            <h1>{{ title }}</h1>
            <h2>{{ subtitle }}</h2>
            <button><h3>{{ buttonText }}</h3></button>
        </div>
    </div>
</template>

<style scoped>
    .organizer {
        background-color: rgba(0, 0, 0, 0.5);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100%;
    }

    h1 {
        background-color: rgba(0, 0, 0, 0.3);
        padding: 20px 0;
        width: 100%;
        text-align: center;
        color: white;
        font-size: 4em;
        margin-bottom: 5px;
    }

    h2{
        color: rgba(255, 255, 255, 0.9);
        background-color: rgba(0, 0, 0, 0.4);
        width: 100%;
        text-align: center;
        padding: 20px 0;
        font-size: 1.5em;
    }

    button {
        width: 400px;
        height: 70px;
        background-color: rgb(0, 128, 0);
        transition: background-color 100ms;
        border-radius: 30px;
        opacity: 1;
        border-color: rgba(0, 0, 0, 0.8);
    }

    button:hover {
        background-color: rgb(0, 100, 0);
    }

    h3 {
        margin: 0;
        font-size: 1.3em;
        color: white;
    }
</style>