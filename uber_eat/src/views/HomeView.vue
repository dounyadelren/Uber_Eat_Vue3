<script setup>
import RestoRow from "../components/RestoRow.vue"
</script>

<template>
  <main>
    <RestoRow v-for="(card, index) in 3" :key="index" />
  </main>
</template>
<style>
</style>
