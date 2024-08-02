<script>

import '@fortawesome/fontawesome-free/css/all.css';

import {store} from '../store.js';

import AppContainer from '../components/AppContainer.vue';

export default {
  name: 'App',
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
      <router-view />
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
  background-image: linear-gradient(to bottom, #eceff1 0%, #72a800 100%);
}

</style>
