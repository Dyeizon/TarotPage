<script>
import CloseButton from './CloseButton.vue';

export default {
    components: {
        CloseButton
    },

    data() {
        return {
            activeItemID: 'li-home-page'
        }
    },  

    methods: {
        selectMenuItem: function($event) {
            document.getElementById(this.activeItemID).classList.remove('selected');
            this.activeItemID = $event.target.id;
            document.getElementById(this.activeItemID).classList.add('selected');
        }
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
                <a href="#"><li id="li-home-page" class="selected" @click="selectMenuItem">Página Inicial</li></a>
                
                <a href="#services"><li id="li-my-arcane" @click="selectMenuItem">Meu arcano</li></a>
                <a href="#services"><li id="li-card-of-the-day" @click="selectMenuItem">Carta do dia</li></a>
                <a href="#services"><li id="li-readings" @click="selectMenuItem">Leituras</li></a>

                <a href="#"><li id="li-online-counsel" @click="selectMenuItem">Consulta online</li></a>
                <a href="#"><li id="li-learning" @click="selectMenuItem">Central do aprendizado</li></a>
                <a href="#"><li id="li-shop" @click="selectMenuItem">Loja</li></a>
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

    #menuContent {
        width: 100%;
        height: 100%;
        transition: width 0.25s, opacity 0.20s linear;
        white-space: nowrap;
    }

    header {
        display: flex;
        justify-content: end;
        align-items: center;
        margin-right: 20px;
        height: 100px;
    }
    
    ul{
        padding-left: 0;
        padding-right: 10px;
        margin: 0;
        width: 100%;
        height: 200px;
    }

    li {
        padding: 10px 0px 10px 20px;
        border-bottom: 1px solid black;
        font-family: 'Poppins', sans-serif;
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

    .selected {
        background-color: rgba(0, 0, 0, 0.2);
    }

</style>

<style>

    .menuTransitions {
        opacity: 0;
        width: 0;
        transition: width 0.5s, opacity 0.5s linear;
    }
</style>