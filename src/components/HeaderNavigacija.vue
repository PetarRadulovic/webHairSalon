<template>
  <img
    @click="sakriNav"
    class="menu"
    src="./photos/menu2.png.jpg"
    alt="menu.png"
  />
  <div ref="navbar" class="nav" v-if="open == true">
    <nav id="nav">
      <ul>
        <li v-for="stavke in nav" :key="stavke.id">
          <a href="#">{{ stavke }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script setup>
import { ref } from "vue";
let nav = ["Pocetna", "Usluga", "Osoblje", "Kontakt", "Lokacija"];
let open = ref(false);
let navbar = ref();
function sakriNav() {
  if (open.value == true) {
    open.value = false;
  } else {
    open.value = true;
  }
}
</script>

<style>
.menu {
  position: absolute;
  position: fixed;
  right: 40px;
  top: 25px;
  width: 50px;
  height: 50px;
  border-radius: 25px;
  opacity: 0.6;
  z-index: 3;
}

#nav {
  position: absolute;
  position: fixed;
  right: 0px;
  top: 0px;
  height: 100vh;
  background-color: goldenrod;
  width: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.nav nav {
  text-align: center;
  font-size: 32px;
}
.nav nav ul {
  display: flex;
  list-style: none;
  flex-direction: column;
  gap: 20px;
}
.nav nav ul li {
  margin-bottom: 15px;
}
.nav nav ul li a {
  text-decoration: none;
  color: #fff;
  cursor: pointer;
}
.nav nav ul li a:hover {
  border-bottom: 2px solid black;
  border-bottom: 10px;
  color: #fff;
}
.nav nav ul li a::after {
  border-bottom: 2px solid black;
}
</style>
