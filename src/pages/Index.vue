<template>
  <div class="cardgroup">
    <game-card :gameId="'zombsroyale'" :art="'https://upload.wikimedia.org/wikipedia/en/6/68/ZombsRoyale.io_Cover_Art.jpg'" />
    <game-card :gameId="'paper'"/>
    <game-card :gameId="'slither'"/>
  </div>

</template>

<style lang="scss">
body {
  background: url("../assets/bg.png");
  padding: 50px;
}
.cardgroup {
  display: flex;
  justify-content: center;

  * {
    margin: 0.25vw;
  }

}
</style>

<script>
import { defineComponent } from 'vue';
import GameCard from '../components/GameCard.vue';

export default defineComponent({
  name: 'PageIndex',
  components: {
    'game-card': GameCard,
  },
});

// export default {
//   name: 'App',
//   components: {
//     'game-card': GameCard,
//   }
// }

</script>
