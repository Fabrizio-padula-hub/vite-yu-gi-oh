<script>
import axios from 'axios';
import { store } from "./store.js";
import AppHeader from "./components/AppHeader.vue";
import CharactersList from "./components/CharactersList.vue";


export default {
  components:{
    AppHeader,
    CharactersList,
  },
  data() {
    return{
      store
    };
  },
  methods: {
    getCharactersApi(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
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
    
    <CharactersList></CharactersList>

  </main>

</template>

<style lang="scss">
@use './style/generic';

</style>
