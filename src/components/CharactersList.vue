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
            <div class="black-bar"></div>
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

        .black-bar{
            width: 100%;
            height: 50px;
            background-color: #222529;
        }

        .single-card{
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 10px;
        }
    }
}
</style>