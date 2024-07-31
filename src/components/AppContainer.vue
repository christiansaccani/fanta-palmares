<script>
import {store} from '../store.js';

import AppBoard from './AppBoard.vue';

export default {

    name: 'AppContainer',

    data() {
        return {
            store
        };
    },

    components: {
    AppBoard,
  },

    methods: {

    }

}
</script>

<!-- ---------------------------------------------------------------------------------- -->

<template>

<section>

  <h1>Classifica Palmarès</h1>

  <div id="container">
    <AppBoard></AppBoard>
  </div>

</section>

</template>

<!-- ---------------------------------------------------------------------------------- -->

<style lang="scss" scoped>

@use '../style/variables' as *;
@use '../style/mixins' as *;

section {

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;

  width: 100%;

  #container {
  width: 80%;

  background-color: whitesmoke;

  border: 4px solid black;
  border-radius: 50px;
 }
}


</style>