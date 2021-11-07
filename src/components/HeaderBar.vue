
<template>
    <div id="background">
      <div id="logo">
      </div>
      <div id="userMenu">
        <UserMenu/>
      </div>
    </div>
</template>

<script>
import UserMenu from "./UserMenu.vue";

export default {
  name: 'HeaderBar',
  components: {
    UserMenu
  }
}
</script>

<style scoped>
#background {
  display: block;
  min-height: 60px;
  width: 100%;
  background: #002244;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

#userMenu {
  margin: 15px;
}
</style>