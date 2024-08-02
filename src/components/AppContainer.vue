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

  <h1>PALMARÈS</h1>

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

  h1 {
    background-color: #fff1eb8a;
    border: 4px solid rgba(0, 0, 0, 0.5);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);

    padding: .5rem 9rem;
    border-radius: 40px;

    font-size: 50px;
    letter-spacing: 3px;
  }

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;

  width: 100%;

    #container {
    width: 80%;

    background-color: #fff1eb8a;

    border: 4px solid rgba(0, 0, 0, 0.5);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    border-radius: 50px;
    }
}

.Btn {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 45px;
  height: 45px;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition-duration: .3s;
  box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.199);
  background-color: #313638;

  position: absolute;
  top: 10px;
  left: 10px;
}

.Btn:nth-of-type(2) {
  position: absolute;
  top: 65px;
  left: 10px;
}

.Btn:nth-of-type(3) {
  position: absolute;
  top: 120px;
  left: 10px;
}

.Btn:last-of-type {
  position: absolute;
  top: 175px;
  left: 10px;

  background-color: rgb(255, 65, 65);
}

/* plus sign */
.sign {
  width: 100%;
  transition-duration: .3s;
  display: flex;
  align-items: center;
  justify-content: center;
}

.sign svg {
  width: 17px;
}

.sign svg path {
  fill: white;
}
/* text */
.text {
  position: absolute;
  right: 0%;
  width: 0%;
  opacity: 0;
  color: white;
  font-size: 1.2em;
  font-weight: 600;
  transition-duration: .3s;
}
/* hover effect on button width */
.Btn:hover {
  width: 135px;
  border-radius: 40px;
  transition-duration: .3s;
}

.Btn:hover .sign {
  width: 30%;
  transition-duration: .3s;
  padding-left: 20px;
}
/* hover effect button's text */
.Btn:hover .text {
  opacity: 1;
  width: 70%;
  transition-duration: .3s;
  padding-right: 10px;
}
/* button click effect*/
.Btn:active {
  transform: translate(2px ,2px);
}

</style>