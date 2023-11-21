<template>
  <div>

    <header>
      <HeaderComponent/>
    </header>

    <main>
      <MainComponent/>
    </main>

    <footer>
      <FooterComponent/>
    </footer>


  </div>
</template>

<script>
  import { store } from './data/store.js';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';

  export default {
    components: {
      HeaderComponent,
      MainComponent,
      FooterComponent
    },


  }
</script>

<style lang="scss" scoped>

</style>