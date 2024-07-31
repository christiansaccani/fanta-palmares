<script>
import { store } from '../store.js';

export default {
  name: 'AppBoard',

  data() {
    return {
      store
    };
  },

  computed: {
    sortedSquadre() {
      return [...this.store.squadre].sort((a, b) => {
        // Ordinamento per campionati, coppe, secondo posto, stagioni
        return (
          b.campionati - a.campionati || // Ordinamento decrescente per campionati
          b.coppe - a.coppe || // Ordinamento decrescente per coppe
          b.sec - a.sec || // Ordinamento decrescente per secondo posto
          a.stagioni - b.stagioni // Ordinamento crescente per stagioni
        );
      });
    }
  }
}
</script>

<!-- ---------------------------------------------------------------------------------- -->

<template>

<div>
    <ul>
      <li>Campionato <div id="scudetto"></div></li>
      <li>Coppa <div id="coppa"></div></li>
      <li>Secondo <div id="secondo">II</div></li>
      <li>Terzo <div id="terzo">III</div></li>
    </ul>
    <div id="scoreboard">
        <div v-for="squadra in sortedSquadre" :key="squadra.nome" class="row">
            <div class="slot" style="width: calc(80% - 211.08px - 144.11px - 170.75px - 132.19px);">
                <strong>{{ squadra.nome }}</strong>
            </div>
            <!-- Slot 2: Campionati -->
            <div class="slot" style="width: 211.08px;">
                <strong>{{ squadra.campionati }}</strong>
            </div>
            <!-- Slot 3: Coppe -->
            <div class="slot" style="width: 144.11px;">
                <strong>{{ squadra.coppe }}</strong>
            </div>
            <!-- Slot 4: Secondo Posto -->
            <div class="slot" style="width: 170.75px;">
                <strong>{{ squadra.sec }}</strong>
            </div>
            <!-- Slot 5: Terzo Posto -->
            <div class="slot" style="width: 132.19px;">
                <strong>{{ squadra.ter }}</strong>
            </div>
        </div>
    </div>
</div>
</template>

<!-- ---------------------------------------------------------------------------------- -->

<style lang="scss" scoped>

@use '../style/variables' as *;
@use '../style/mixins' as *;

div {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;

    ul {
        display: flex;
        width: 100%;

        justify-content: flex-end;
        margin-top: 2rem;
        padding-right: 10rem;

        gap: 5rem;

        list-style: none;

        li {
            font-size: 26px;
            font-weight: 700;

            display: flex;
            align-items: center;
            gap: 1rem;

            #scudetto {
                height: 50px;
                width: 46px;
                background: linear-gradient(to right, green 33.33%, white 33.33%, white 66.66%, red 66.66%);

                border-bottom-left-radius: 50%;
                border-bottom-right-radius: 50%;
                border: 2px solid gold;
            }

            #coppa {
                height: 50px;
                width: 50px;
                background: radial-gradient(circle, green 25%, white 25%, white 50%, red 50%);

                border-radius: 50%;
                border: 2px solid gold;
            }

            #secondo {
                display: grid;
                place-items: center;

                height: 50px;
                width: 50px;
                background-color: #c2c2c2;
                color: #565454;

                border-radius: 50%;
                border: 2px solid #565454;
            }

            #terzo {
                display: grid;
                place-items: center;

                height: 50px;
                width: 50px;
                background-color: #d99c71;
                color: #76431f;

                border-radius: 50%;
                border: 2px solid #76431f;
            }
        }
    }

    // 132,19
    #scoreboard {
        width: 85%;
        margin-bottom: 2rem;

        .row {
            display: flex;
            flex-direction: row;
            gap: 5rem;

            justify-content: flex-end;
            align-items: center;

            width: 100%;
            height: 40px;

            margin-right: .2rem;

            .slot {
                font-size: 24px;      
                border-left: 1px solid black;   
                border-right: 1px solid black;      
            }
        }
    }
}

</style>