<script>
export default {
    data (){
        return {
            categoriesList: ['Alien', 'Frog', 'Shaddoll', 'Eldlich', 'Nekroz', 'Umi'],
            selected: null,
        }
    }
}

</script>

<template>
    <div class="container-fluid d-flex justify-content-center">
        <div class="row">
                <select name="" id="" class="form-select" v-model="selected" @change="$emit('selectedCharacter', selected)">
                    <option disabled value="">Seleziona una categoria</option>
                    <option v-for="archetypes in categoriesList"> {{ archetypes }} </option>
                </select>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #select-container{
        background-color: white;
        border-radius: 10px;
        width: 400px;
    }
</style>