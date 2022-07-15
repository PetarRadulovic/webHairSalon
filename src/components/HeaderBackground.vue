<template>
  <div class="slika">
    <h1 id="slika_naslov">Salon Joja</h1>
    <img src="./photos/img.background.jpg" alt="backgroundImg" />
  </div>
</template>
<script setup></script>

<style>
.slika {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column-reverse;
}
#slika_naslov {
  font-size: 45px;
  position: absolute;
  color: goldenrod;
  display: block;
  border-bottom: 2px solid goldenrod;
}
.slika img {
  background-size: cover;
  background-position: center;

  height: 100vh;
  width: 100%;
}
</style>
