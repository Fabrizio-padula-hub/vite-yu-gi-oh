<script>
import { store } from "../store.js";
import CharactersCard from "./CharactersCard.vue";

export default{
    name: 'CharactersList',
    components:{
    CharactersCard
  },
  data(){
    return{
        store
    };
  }
}
</script>

<template>

    <section class="characters">
        <div class="container">
            <div class="single-card">
                <CharactersCard v-for="character in store.characters" :key="character.id" :infoCard="character"></CharactersCard>
            </div>
            
        </div>
        
    </section>

</template>

<style scoped lang="scss">
.characters{
    background-color: #d59038;
    padding: 40px 0;

    .container{
        background-color: #fff;
        padding: 20px;

        .single-card{
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
    }
}
</style>