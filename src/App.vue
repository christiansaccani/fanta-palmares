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
  background-image: linear-gradient(to top, #fff1eb 0%, #ace0f9 100%);
}

</style>
