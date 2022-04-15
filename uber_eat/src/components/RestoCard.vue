<template>
    <div class="restaurant-card">
        <div class="restaurant-image"></div>
        <div class="restaurant-info">
            <div class="top">
                <p class="name">{{ info_resto.name}}</p>
                <p class="note"><span>{{ info_resto.note}}</span></p>
            </div>
        </div>
        <p class="time">{{ info_resto.drive_time }}</p>
    </div>
</template>

<script>
export default {
    name:
    'RestoCard',
    props: {
        info_resto: Object
    }

}
</script>

<style lang="scss">
.restaurant-card {
    width: 32%;
    height: 30vh;

    p {
        margin: 0px;
    }
}

.restaurant-image {
    background-image: url();
    height: 70%;
    background-size: cover;
    background-position: center;
}

.restaurant-info {
    .top {
        margin: 10px 0px;
        display: flex;
        justify-content: space-between;
        .note {
            background-color: #eeeeee;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 30px;
            width: 30px;
            font-size: 0.8rem;
            border-radius: 50%;
        }
    }
    .time {
        font-size: 0.9rem;

    }
}
</style>