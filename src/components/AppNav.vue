<script>
import {store} from '../store.js';

export default {

    name: 'AppNav',

    data() {
        return {
            store
        };
    },
    methods: {
    scrollToSkills(event) {
      event.preventDefault(); // Previeni il comportamento predefinito del click
      window.scrollTo({
        top: 785,
        behavior: 'smooth' // Effetto di scorrimento fluido
      });
    },
    scrollToContacts(event) {
      event.preventDefault(); // Previeni il comportamento predefinito del click
      const totalHeight = document.body.scrollHeight;

      window.scrollTo({
        top: totalHeight,
        behavior: 'smooth' // Effetto di scorrimento fluido
      });
    },
    }

}
</script>

<!-- ---------------------------------------------------------------------------------- -->

<template>



</template>

<!-- ---------------------------------------------------------------------------------- -->

<style lang="scss" scoped>

@use '../style/variables' as *;
@use '../style/mixins' as *;



</style>