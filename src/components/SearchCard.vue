<script>
import axios from 'axios';

export default{
    name: 'SearchCard',
    data(){
        return{
            archetipoStatus: []
        };
    },
    methods: {
    getarchetipoApi(){
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
      .then((response) => {
        this.archetipoStatus = response.data;
      });
    }
    },
    mounted(){
        this.getarchetipoApi();
    }

}
</script>

<template>
    <div class="container">
        <select name="" class="app-search">
            <option v-for="archetipo in archetipoStatus">{{ archetipo.archetype_name }}</option>
        </select>
    </div>

</template>

<style scoped lang="scss">
.app-search{
    margin-bottom: 20px;
    font-size: 18px;
    padding: 0px 12px;
}

</style>