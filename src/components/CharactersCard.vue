<script>
export default{
    name: 'CharactersCard',
}
</script>

<template>
    <div class="card">
        <div>
            <img src="https://images.ygoprodeck.com/images/cards_small/34541863.jpg" alt="">
        </div>
        <h4>Prova titolo card</h4>
        <div class="subtitle">
            Prova sottotitolo
        </div>
    </div>
</template>

<style scoped lang="scss">
.card{
    background-color: #d59038;
    width: calc((100% / 5) - 10px);
    text-align: center;

    img{
        width: 100%;
    }

    h4{
        margin: 8px 0;
    }

    .subtitle{
        margin: 12px 0;
    }
}
</style>