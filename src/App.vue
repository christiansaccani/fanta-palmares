<script>

import '@fortawesome/fontawesome-free/css/all.css';

import {store} from './store.js';

import AppNav from './components/AppNav.vue';

export default {

  data() {
    return {
      store,
    }
  },

  components: {
    AppNav,
  },
}

</script>

<template>
  
  <body>
    <AppNav></AppNav>

  </body>
  
</template>

<style lang="scss" scoped>

body {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center !important;

 
}

</style>

<!-- 

Cose da fare:
 
- Inserisci la sezione dedicata ai progetti
- Inserisci il toggle per la lingua
- Inserisci le traduzione
- Decidi i colori da usare

-->