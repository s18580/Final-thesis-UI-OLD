
<template>
    <div id="background">
      <nav>
        <ul>
          <li v-if="hasRole()">
            <router-link :to="{name: 'Home'}" exact>
              <div class="menuLink">
                Strona główna - Admin
              </div>
            </router-link>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Zarządzanie kontami
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Stałe programowe
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Kopie zapasowe
            </div>
          </li>
          <li v-if="hasRole()">
            <router-link :to="{name: 'Home'}" exact>
              <div class="menuLink">
                Strona główna - Pracownik
              </div>
            </router-link>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Zamówienia
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Klienci
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Dostawcy
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Wyceny
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Pracownicy
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Statystyki
            </div>
          </li>
          <li v-if="hasRole()">
            <div class="menuLink">
              Wyszukaj osobę kontaktową
            </div>
          </li>
          <li v-if="hasRole()">
            <router-link :to="{name: 'Home'}" exact>
              <div class="menuLink">
                Strona główna - Księgowa
              </div>
            </router-link>
          </li>
        </ul>
      </nav>
    </div>
</template>

<script>

export default {
  name: 'MenuBar',
  methods: {
    hasRole: function(){
      return true; //ToDo: checking role in VueX store
    }
  }
}
</script>

<style scoped>
#background {
  min-width: 200px;
  height: 100%;
  position: fixed;
  background: linear-gradient(to right top, #000000, #007FFF);
}
.menuLink{
  padding: 15px;
  color: white;
  text-align: center;
  border-bottom: 0.1rem solid black;
}

#background ul{
  padding: 0;
  margin: 0;
}

#background ul li{
  list-style-type: none;
}
</style>