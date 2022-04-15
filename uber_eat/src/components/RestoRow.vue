<template>
    <div class="restaurant-row">
        <h2 class="title">Nos restaurants</h2>
        <div class="wrapper-card">
            <RestoCard v-for="(card, index) in 3" :key="index" />
        </div>
    </div>

</template>

<script>
import RestoCard from "./RestoCard.vue"
export default {
    name: "RestoRow",
    components: "RestoCard",
    components: { RestoCard }
}
</script>

<style lang="scss">
.restaurant-row {
    .wrapper-card {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}
</style>