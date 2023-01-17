<script>
import Menu from '../Menu/Menu.vue';
import MenuIcon from './icons/MenuIcon.vue';
import Logo from './icons/LogoIcon.vue';
import Search from './icons/SearchIcon.vue';
import Login from './icons/LoginIcon.vue';

export default {
  data() {
    return {
      isMenuActive: false
    }
  },

  components: {
    Menu,
    MenuIcon,
    Logo,
    Search,
    Login,
  },
  methods: {
    openMenu: function() {
      this.isMenuActive = true;
      document.getElementById('menu').style.width = "300px";
      document.getElementById('menuContent').style.opacity = "1";
    },

    closeMenu: function() {
      document.getElementById('menu').style.width = "0px";
      document.getElementById('menuContent').style.opacity = "0";
      

      setTimeout(() => {
        this.isMenuActive = false;
      }, 500)
    }
  }
}
</script>

<template>
  <header class="sticky-top">
    <div class="container h-alignment">
      <Menu id="menu" @closeMenu="closeMenu" class="menu menuTransitions" :class="{'showMenu' : isMenuActive}"/>
      <MenuIcon @openMenu="openMenu" :class="{'hideMenuIcon': isMenuActive}"/>
      <Logo/>
      <Search/>
      <Login/>
    </div>
  </header>
</template>

<style scoped>
  header {
    background-color: #FFFDFA;
    height: 100px;
    display: flex;
    align-items: center;

    border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    box-shadow: 0px 0px 5px 3px rgba(0, 0, 0, 0.2);

    position: sticky;
    position: -webkit-sticky;
  }

  .h-alignment {
    display: flex;
    align-items: center;
  }

  .hideMenuIcon {
    visibility: hidden;
  }

  .showMenu {
    visibility: visible;
  }
</style>