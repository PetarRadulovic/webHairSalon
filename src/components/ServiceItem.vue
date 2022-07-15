<template>
  <div id="services">
    <h1 id="uslugeNaslov">{{ naslov }}</h1>
    <nav id="UslugeItem">
      <ul>
        <li
          v-for="item in usluge"
          :key="item.id"
          ref="item"
          @click="ispisiUsluge"
        >
          {{ item }}
        </li>
      </ul>
    </nav>
  </div>
</template>

<script setup>
import { ref } from "vue";
defineProps({
  naslov: String,
  usluge: Array,
});
let usluge = [`Nails`, `HairStyle`, `Makeup`, `Airbrush`];
let show = ref(false);
function ispisiUsluge() {
  console.log(show.value);
}
</script>

<style>
#services {
  display: flex;
  flex-direction: column;
  row-gap: 20px;
  background-color: #e3e3e3;
}
#uslugeNaslov {
  margin-top: 10px;
  padding: 7px;
  font-size: 30px;
  color: goldenrod;
}
#uslugeNaslov:hover {
  background-color: black;
  border-radius: 10px;
}
#UslugeItem {
  width: 80%;
  display: inline;
}
nav ul {
  list-style: none;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
nav ul li {
  padding: 10px;
  margin-bottom: 10px;
}
nav ul li {
  color: goldenrod;
}
nav ul li:hover {
  background-color: black;
  border-radius: 10px;
}
</style>
