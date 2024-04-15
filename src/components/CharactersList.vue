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
            <div class="card">
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

        .card{
        display: flex;
        flex-wrap: wrap;
    }
    }

    
}



</style>