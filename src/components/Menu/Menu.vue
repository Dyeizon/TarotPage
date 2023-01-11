<script>
import CloseButton from './CloseButton.vue';

export default {
    components: {
        CloseButton
    }
}
</script>

<template>
    <aside>
        <header>
            <CloseButton @click="$emit('closeMenu')"/>
        </header>
        <div id="menuContent" class="menuTransitions">
            <h1>teste</h1>
        </div>
    </aside>
</template>

<style scoped>
    aside {
        position: absolute;
        top: 0;
        left: 0;
        width: 0;
        height: 100vh;
        background-color: #f9d366;
        opacity: 0.95;
        z-index: 1;
        visibility: hidden;
    }

    header {
        display: flex;
        justify-content: end;
        margin-top: 20px;
        margin-right: 20px;
    }
</style>

<style>
    .menuTransitions {
        opacity: 0;
        width: 0;
        transition: width 0.5s, opacity 1s linear;
    }
</style>