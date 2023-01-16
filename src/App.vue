<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

import {store} from './store';
import axios from 'axios';

export default {
  components:{
    AppHeader,
    AppMain
  },
  data(){
    return{
      store 
    }
  },
  created(){
    this.getCards();
  },
  methods:{
    getCards(){
      axios.get(store.url).then((response) => {
        store.cardsList.vue = response.data.data;
      });
    }
  }
}
</script>

<template lang="">
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
  @use './styles/generals.scss'
  
</style>