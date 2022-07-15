<template>
  <div ref="info" id="info">
    <h2 class="info_naslov">{{ tipUsluge }}</h2>
    <img class="info_slika" :src="slika" :alt="slika" />
    <p class="info_tekst">{{ tekst }}</p>
  </div>
</template>

<script setup>
import { ref } from "vue";

let info = ref();

defineProps({
  tipUsluge: String,
  slika: String,
  tekst: String,
});
</script>

<style>
#info {
  margin-top: 10px;
  padding: 10px;
  width: 50%;
  display: flex;
  flex-direction: column;
  background-color: #e3e3e3;
}
.info_slika {
  width: 350px;
  height: 400px;
  border-radius: 20px;
}

.info_naslov {
  padding: 5px;
  margin: 10px;
  color: goldenrod;
  text-align: center;
}
.info_tekst {
  padding: 5px;
  margin: 10px;
  color: black;
  text-align: center;
  font-size: medium;
}
</style>
