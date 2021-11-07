<template>
  <div id="header">
    <HeaderBar/>
  </div>
  <div id="menu">
    <MenuBar/>
  </div>
  <div id="content">
    <div>Icons made by <a href="https://www.flaticon.com/authors/payungkead" title="Payungkead">Payungkead</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
  </div>
</template>

<script>
import MenuBar from './components/MenuBar.vue';
import HeaderBar from './components/HeaderBar.vue';

export default {
  name: 'App',
  components: {
    MenuBar,
    HeaderBar
  }
}
</script>

<style>
#app {
  display: grid;
  grid-template-columns: 1fr 8fr;
  grid-template-rows: auto;
  grid-template-areas: 
    "header header"
    "menu content";
}

body {
  margin: 0;
  padding: 0;
}

#menu {
  grid-area: menu;
}

#header {
  grid-area: header;
}

#content {
  grid-area: content;
}
</style>
