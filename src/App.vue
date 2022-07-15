<template>
  <main>
    <HeaderBackground />
    <HeaderNavigacija />
    <ServiceItem :naslov="`Usluge`" />
    <InfoUsluge
      v-for="item in list"
      :key="item.id"
      :tip-usluge="item.title"
      :slika="item.imgsrc"
      :tekst="item.text"
    />

    <div id="osobljeInfo">
      <h2 class="osobljeInfo_naslov">Osoblje</h2>
      <OsobljeInfo
        v-for="osoba in listaosoblja"
        :key="osoba.id"
        :ime="osoba.ime"
        :slika="osoba.imgsrc"
      />
    </div>
  </main>
</template>

<script setup>
import HeaderBackground from "./components/HeaderBackground.vue";
import HeaderNavigacija from "./components/HeaderNavigacija.vue";
import ServiceItem from "./components/ServiceItem.vue";
import InfoUsluge from "./components/InfoUsluge.vue";
import list from "./assets/stavke.poslova.json";
import OsobljeInfo from "./components/OsobljeInfo.vue";
import listaosoblja from "./assets/osoblje.json";
</script>
<style>
* {
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  background-color: #e3e3e3;
}
#osobljeinfo {
  display: flex;
  flex-direction: column;
  row-gap: 20px;
  background-color: #e3e3e3;
}
#osobljeInfo .osobljeInfo_naslov {
  text-align: center;
  margin-top: 10px;
  padding: 7px;
  font-size: 30px;
  color: goldenrod;
}
</style>
