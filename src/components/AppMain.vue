<script>
import { store } from '../store.js';
import CardsList from './CardsList.vue';
import SelectType from './SelectType.vue';
import axios from 'axios';

export default {
    components:{
        SelectType,
        CardsList
    },
    data() {
        return {
            store,
        }
    },
    methods: {
        searchedCharacter(selectedCategory){
            axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=${selectedCategory}`, {
              params: {
                category: selectedCategory,
              }
            })
            .then((response) => {
                this.store.cardsList = response.data.data; 
            })
        }
    },
    
}
</script>

<template lang="">
    <main>
        <div class="row">
            <div class="col-2">
                <SelectType
            @selectedCharacter="searchedCharacter"/>
            </div>
            <div class="col-10"></div>
        </div>
        <CardsList />
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;

    main{
        padding: 50px 10%;
    }
    
</style>