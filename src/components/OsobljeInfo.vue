<template>
  <div class="osoblje">
    <h1 class="osoblje_naslov">{{ ime }}</h1>
    <img class="osoblje_slika" :src="slika" />
    <p class="osoblje_tekst">{{ tekst }}</p>
  </div>
</template>

<script setup>
defineProps({
  ime: String,
  slika: String,
  tekst: String,
});
</script>

<style>
.osoblje {
  display: inline-grid;
  width: 50%;
  text-align: center;
  row-gap: 15px;
}
.osoblje_slika {
  width: 250px;
  height: 250px;
  border-radius: 20px;
}
</style>
