<script>
import axios from 'axios';
import { store } from "../store.js";

export default{
    name: 'SearchCard',
    data(){
        return{
            store,
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
        <select @change="$emit('cardSearchArchetipo')" v-model="store.searchArchetipo" class="app-search">
            <option value="">Scegli un argomento</option>
            <option v-for="archetipo in archetipoStatus" value="archetipo.archetype_name">
                {{ archetipo.archetype_name }}
            </option>
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