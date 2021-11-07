
<template>
    <button class="icon" @click="this.showHideMenu()"></button>
    <div class ="userMenu" v-show="isMenuOpen">
        <ul>
            <li>Zmień hasło</li>
            <li>Wyloguj</li>
        </ul>
    </div>
</template>

<script>

export default {
  name: 'UserMenu',
  data: function() {
      return {
        isMenuOpen: false,
      }
  },
  methods: {
      showHideMenu: function(){
        this.isMenuOpen = !this.isMenuOpen;
      }
  }
}
</script>

<style scoped>
.icon {
  background: url(../assets/userIcon.png) no-repeat;
  cursor:pointer;
  height: 32px;
  width: 32px;
  outline: none;
  border: 0px;
  color: white;
}

.userMenu {
  position: absolute;
  right:10px;
  display: flex;
  background: black;
}

.userMenu ul {
  padding: 0;
  margin: 0;
}

.userMenu ul li {
  list-style-type: none;
  display: block;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 8px;
  padding-right: 8px;
  text-align: center;
  color: white;
}
</style>