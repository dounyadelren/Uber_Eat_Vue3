<script>
import RestoRow from "../components/RestoRow.vue"
import Bdd from "../bdd.js"
import { onMounted, ref } from "vue"

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

    let dataResto = ref([]);
    let three_resto = []
    const makeDataRestaurant = () => {
      for (const restaurant of Bdd) {
        const new_resto = new Restaurant(restaurant.name, restaurant.note, restaurant.image, restaurant.drive_time);
        if (three_resto.length === 2) {
          three_resto.push(new_resto);
          dataResto.value.push(three_resto);
          three_resto = []
        } else {
          three_resto.push(new_resto)
        }
      }
    }
    onMounted(makeDataRestaurant);
    return {
      dataResto
    }
  }
}
</script>

<template>
  <main>
    <RestoRow v-for="(data, i) in dataResto" v-bind:key="i" :three_resto="data"/>
  </main>
</template>
<style>
</style>
