<script>

import '@fortawesome/fontawesome-free/css/all.css';

import {store} from './store.js';

import AppContainer from './components/AppContainer.vue';

export default {

  data() {
    return {
      store,
    }
  },

  components: {
    AppContainer,
  },
}

</script>

<template>
  
  <body>
    <AppContainer>
      
    </AppContainer>
  </body>
  
</template>

<style lang="scss" scoped>

body {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: whitesmoke;
}

</style>