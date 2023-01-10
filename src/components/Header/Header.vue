<script>
import Menu from './icons/MenuIcon.vue';
import Logo from './icons/LogoIcon.vue';
import Search from './icons/SearchIcon.vue';
import Login from './icons/LoginIcon.vue';

export default {
    components: {
      Menu,
      Logo,
      Search,
      Login
    }
}
</script>

<template>
  <header class="sticky-top">
    <div class="container h-alignment">
      <Menu/>
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
    top: 0px;
  }

  .h-alignment {
    display: flex;
    align-items: center;
  }
</style>