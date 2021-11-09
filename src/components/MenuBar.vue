
<template>
    <div id="background">
      <ul>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Strona główna - Admin
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Zarządzanie kontami
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Stałe programowe
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Kopie zapasowe
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Strona główna - Pracownik
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Zamówienia
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Klienci
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Dostawcy
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Wyceny
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Pracownicy
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Statystyki
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Wyszukaj osobę kontaktową
          </div>
        </li>
        <li>
          <div v-if="hasRole()" class="menuLink">
            Strona główna - Księgowa
          </div>
        </li>
      </ul>
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