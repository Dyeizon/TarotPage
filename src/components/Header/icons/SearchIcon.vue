<script>
  export default {
    data() {
      return {
        isSearchBarActive: false
      }
    },
    methods: {
      toggleSearchBar: function() {
        this.isSearchBarActive = !this.isSearchBarActive;        
        this.$nextTick(() => {
          this.$refs.searchBar.focus();
        })
      }
    }
  }
</script>

<template>
<div>
  <input id="teste" ref="searchBar" :class="{'displaySearchBar' : isSearchBarActive}" type="search">
  <button @click="toggleSearchBar">

    <svg
        xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
        xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        xmlns:ns1="http://sozi.baierouge.fr"
        xmlns:cc="http://creativecommons.org/ns#"
        xmlns:dc="http://purl.org/dc/elements/1.1/"
        xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
        id="Layer_1"
        viewBox="0 0 46.553307 46.200966"
        width="24px"
        height="24px"
        version="1.1"
        fill="#7a36be"
      >
      <g transform="translate(-29.461,-26.738)">
        <path
            d="m69.902 72.704-10.935-10.935c-2.997 1.961-6.579 3.111-10.444 3.111-10.539 0-19.062-8.542-19.062-19.081 0-10.519 8.522-19.061 19.062-19.061 10.521 0 19.06 8.542 19.06 19.061 0 3.679-1.036 7.107-2.828 10.011l11.013 11.011c0.583 0.567 0.094 1.981-1.076 3.148l-1.64 1.644c-1.17 1.167-2.584 1.656-3.15 1.091zm-8.653-26.905c0-7.033-5.695-12.727-12.727-12.727-7.033 0-12.745 5.694-12.745 12.727s5.712 12.745 12.745 12.745c7.032 0 12.727-5.711 12.727-12.745z"
        />
      </g>
    </svg>
  </button>
</div>
</template>

<style scoped>
  div {
    position: relative;
    display: flex;
    align-items: center;
  }

  button {
    background-color: transparent;
    border: none;
  }

  input {
    visibility: hidden;
    border: 1px solid rgba(122, 54, 190, 0.2);
    border-radius: 5px;
    border-top-left-radius: 15px;
    border-bottom-left-radius: 15px;
    padding: 5px;
    padding-left: 15px;
    caret-color: rgba(0, 0, 0, 0.5);
    background-color: rgba(122, 54, 190, 0.1);
    opacity: 0;
    transition: opacity 200ms;

    position: absolute;
    left: -210px;

  }

  /* clears the ‘X’ from Internet Explorer */
  input[type=search]::-ms-clear { display: none; width : 0; height: 0; }
  input[type=search]::-ms-reveal { display: none; width : 0; height: 0; }
  /* clears the ‘X’ from Chrome */
  input[type="search"]::-webkit-search-decoration,
  input[type="search"]::-webkit-search-cancel-button,
  input[type="search"]::-webkit-search-results-button,
  input[type="search"]::-webkit-search-results-decoration { display: none; }

  input:focus {
    outline: none;
  }

  .displaySearchBar {
    visibility: visible;
    opacity: 1;
  }
</style>