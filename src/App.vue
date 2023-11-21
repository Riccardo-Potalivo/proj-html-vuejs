<template>
  <div>

    <header>
      <HeaderComponent/>
    </header>

    <main>
      <MainComponent/>
    </main>


  </div>
</template>

<script>
  import { store } from './data/store.js';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';

  export default {
    components: {
      HeaderComponent,
      MainComponent
    },


  }
</script>

<style lang="scss" scoped>

</style>