<script>
import AppHeader from "./components/AppHeader.vue";
import CharactersList from "./components/CharactersList.vue";


export default {
  components:{
    AppHeader,
    CharactersList,
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
