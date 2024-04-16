<script>
import axios from 'axios';
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import SearchCard from "./components/SearchCard.vue";
import CharactersList from "./components/CharactersList.vue";


export default {
  components:{
    AppHeader,
    CharactersList,
    SearchCard
  },
  data() {
    return{
      store
    };
  },
  methods: {
    getCharactersApi(){
      let apiUrl = 'https://db.ygoprodeck.com/api/v7/cardinfo.php'

      const queryParams = {
        num: 20,
        offset: 0,
        archetype: ''
      }
      // if(store.searchArchetipo !== ''){
      //   queryParams.archetype = store.searchArchetipo;
      // }


      axios.get(apiUrl,{
        params: queryParams 
      })
      .then((response) => {
        store.characters = response.data.data;
      });
    }
  },
  mounted(){
    this.getCharactersApi();
  }


}

</script>

<template>
  <AppHeader></AppHeader>

  <main>
    <SearchCard  @cardSearchArchetipo="getCharactersApi"></SearchCard>
    <CharactersList></CharactersList>

  </main>

</template>

<style lang="scss">
@use './style/generic';

</style>
