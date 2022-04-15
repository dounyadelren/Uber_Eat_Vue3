<script setup>
import { RouterLink, RouterView } from "vue-router";
import RestoCard from "./components/RestoCard.vue";

</script>

<template>
  <header>
    <RestoCard />
  </header>

  <RouterView />
</template>
<style>
@import url('./assets/styles/reset.css');
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');

#app {
  font-family: "Roboto", sans-serif;
}
</style>

