<script>
import MenuIconSVG from './MenuIconSVG.vue';
export default {
    components: {
        MenuIconSVG,
    }
}
</script>

<template>
    <button @click="this.$emit('openMenu');">
        <MenuIconSVG/>
    </button>
</template>

<style scoped>
    button {
        height: 100%;
        background-color: transparent;
        padding: 12px;
        border: 2px solid #7a36be;
        border-radius: 30px;
    }
</style>

<style>
button {
        opacity: 0.7;
        transition: opacity 200ms;
    }

button:hover {
        opacity: 1;
    }
</style>