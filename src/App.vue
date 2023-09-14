<script setup lang="ts">
import NavbarDash from './components/NavbarDash.vue';
import NavbarTop from './components/NavbarTop.vue';




</script>

<template>
  <NavbarDash />
  <section class="dashboard">
    <NavbarTop />
  </section>
</template>

<style scoped>
@import url('https://unicons.iconscout.com/release/v4.0.8/css/line.css');

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;300;400;500;600&display=swap');

* {
  font-family: 'Poppins', sans-serif;
}

.dashboard {
  position: relative;
  left: 250px;
  background-color: var(--panel-color);
  height: 100vh;
  width: calc(100% - 250px);
  padding: 10px 14px;
  transition: var(--tran-05);
}


nav.close~.dashboard {
  left: 73px;
  width: calc(100% - 73px);
}
</style>
