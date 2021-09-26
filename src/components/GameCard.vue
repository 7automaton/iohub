<template>
  <a :href="gameList[gameId].url">
    <q-card class="mycard bg-black">
      <!-- <p>{{gameList[gameId].art}}</p> yeah man this works fine -->
      <q-img :src="gameList[gameId].art">
      </q-img>
    </q-card>
    <!-- <div class="texts">
      <p class="title">{{gameList[gameId].name}}</p>
    </div> -->
  </a>
</template>

<style lang="scss">
.mycard {
  width: 28vw;
  height: 17vw;
  display: flex;
  flex-grow: 1;
}
.title {
  color: white;
}
</style>

<script>
import gamelist from '../assets/gamelist.json';

export default {
  props: {
    gameId: { required: true, type: String },
    art: { required: true, type: String },
  },
  data() {
    return {
      gameList: gamelist.games,
    };
  },
};
</script>
