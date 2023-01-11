<script>
import CloseButtonSVG from './CloseButtonSVG.vue';

export default {
    components: {
        CloseButtonSVG
    }
}
</script>

<template>
    <button>
        <CloseButtonSVG/>
    </button>
</template>

<style scoped>
    button {
        border: none;
        background-color: transparent;
    }
</style>