<script>
import CardsList from './CardsList.vue';

export default {
    components:{
        CardsList
    },
}
</script>

<template lang="">
    <main>
         <div class="row">
            <div class="col-2">
                <select class="form-select">
                    <option selected>Alien</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                </select>
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

        .select{
            padding: 10px 30px;
        }
    }
    
</style>