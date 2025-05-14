<script setup>
import Nav from './components/Nav.vue';
import Footer from './components/Footer.vue';

</script>

<template>
<Nav></Nav>
<Footer></Footer>
</template>

<style scoped>

@font-face {
  font-family: 'GenRyuMin-B';
  src:
    url('./font/GenRyuMinTW-Bold.ttf') format("truetype"),
    url('./fonts/Helvetica.eot') format("embedded-opentype");
}

@font-face {
  font-family: 'GenRyuMin-R';
  src:
    url('./font/GenRyuMinTW-Regular.ttf') format("truetype"),
    url('./font/GenRyuMinTW-Regular') format("embedded-opentype");
}

@font-face {
  font-family: 'GenRyuMin-M';
  src:
    url('./font/GenRyuMinTW-Medium.ttf') format("truetype"),
    url('./font/GenRyuMinTW-Medium') format("embedded-opentype");
}
</style>
