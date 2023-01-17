<script>
import {store} from '../store';
import SingleCard from './SingleCard.vue'

export default {
    components:{
        SingleCard
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template lang="">
    <div class="card-list-container">
        <div class="card-banner">
            <h5>Found # cards</h5>
        </div> 
        <div class="card-list">
            <SingleCard v-for="(item, index) in store.cardsList" :key="index" :card="item" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .card-list-container{
        background-color: #fff;
        padding: 50px;
        margin-top: 50px;

        .card-banner{
            color: $ygo-white;
            background-color: $ygo-black;
            padding: 20px 30px;
            margin: 0;

            h5{
                margin: 0 !important;
                font-weight: bolder;
            }
        }

        .card-list {
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }
    }
</style>