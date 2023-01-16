<script>
export default {
    props:{
        card: Object
    },
    data(){
        return{
            index: 0
        }
    }
}
</script>

<template lang="">
    <div class="cards-card">
        <div class="cards-img">
            <img :src="card.card_images[0].image_url" />
        </div>
        <div class="cards-text">
            <h3>{{card.name}}</h3>
            <p>{{card.type}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .cards-card{
        background-color: $ygo-orange;

        h3{
            color: $ygo-white;
            text-transform: uppercase;
        }
    }
</style>