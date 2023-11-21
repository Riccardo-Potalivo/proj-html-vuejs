<template>
  <div>
    <HeaderComponent/>

  </div>
</template>

<script>
  import { store } from './data/store.js';
  import axios from 'axios';
  import HeaderComponent from './components/HeaderComponent.vue'

  export default {
    components: {
      HeaderComponent
    },


  }
</script>

<style lang="scss" scoped>

</style>