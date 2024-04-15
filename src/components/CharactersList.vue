<script>
import CharactersCard from "./CharactersCard.vue";

export default{
    name: 'CharactersList',
    components:{
    CharactersCard
  }
}
</script>

<template>

    <section class="characters">
        <div class="container">
            <div class="single-card">
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
                <CharactersCard></CharactersCard>
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