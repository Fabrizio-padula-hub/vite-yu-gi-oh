<script>
export default{
    name: 'CharactersCard',
    props: {
        infoCard: Object
    }
}
</script>

<template>
    <div class="card">
        <div>
            <img :src="infoCard.card_images[0].image_url_small" :alt="infoCard.name">
        </div>
        <h4>{{ infoCard.name }}</h4>
        <div class="subtitle">
            {{ infoCard.archetype }}
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
        color: white;
    }

    .subtitle{
        margin: 12px 0;
    }
}
</style>