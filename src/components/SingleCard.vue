<script>
import { store } from '../store';

export default {
    props:{
        card: Object
    },
    data(){
        return{
            store,
            index: 0
        }
    }
}
</script>

<template>
    <div class="cards-card">
        <div class="cards-img">
            <img :src="card.card_images[0].image_url" />
        </div>
        <div class="cards-text">
            <h6>{{card.name}}</h6>
            <p>{{card.archetype}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .cards-card{
        background-color: $ygo-orange;
        width: 200px;
        text-align: center;
        margin-bottom: 20px;

        img{
            width: 200px;
        }

        h6{
            color: $ygo-white;
            text-transform: uppercase;
            font-weight: 600;
            margin-top: 10px;
        }
    }
</style>