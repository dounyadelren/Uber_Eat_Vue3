<script>
import RestoRow from "../components/RestoRow.vue"
import Bdd from "../bdd.js"

export default {
  name: "HomeView",
  components: {
    RestoRow,
  },
  setup() {
    class Restaurant {
      constructor(name, note, image, drive_time) {
        this.name = name
        this.note = note
        this.image = image
        this.drive_time = drive_time
      }
    }
    var resto = new Restaurant('toto', '3.5', 'url', '30min')
    console.log(resto)
  }
}
</script>

<template>
  <main>
    <RestoRow v-for="(card, index) in 3" :key="index" />
  </main>
</template>
<style>
</style>
