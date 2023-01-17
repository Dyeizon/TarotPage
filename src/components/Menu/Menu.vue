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
            <ul>
                <a href="#"><li>Meu arcano</li></a>
                <a href="#"><li>Carta do dia</li></a>
                <a href="#"><li>Leituras</li></a>
            </ul>
        </div>
    </aside>
</template>

<style scoped>
    aside {
        position: absolute;
        top: 0;
        left: 0;
        width: 0;
        height: calc(100vh);
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
    
    ul{
        padding-left: 0;
        padding-right: 10px;
        margin: 0;
        width: 300px;
        height: 200px;
    }

    li {
        padding: 10px 0px 10px 20px;
        border-bottom: 1px solid black;
    }

    a {
        text-decoration: none;
        color: inherit;
    }

    a:hover {
        color: black;
    }

    a:hover li {
        background-color: rgba(0, 0, 0, 0.1);
    }

</style>

<style>
    .menuTransitions {
        opacity: 0;
        width: 0;
        transition: width 0.5s, opacity 0.30s linear;
    }
</style>