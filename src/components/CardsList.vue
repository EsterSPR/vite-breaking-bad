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
    <div class="card-container">
        <SingleCard v-for="(item, index) in cardsList" :key="index" :card="item" />
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    .card-container{
        background-color: #fff;
        padding: 50px;
        margin-top: 50px;
    }
</style>