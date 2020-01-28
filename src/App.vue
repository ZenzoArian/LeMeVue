<template>
  <div id="app">
    <Games v-bind:games="games" v-on:del-todo="deleteGame" />
  </div>
</template>

<script>
import Games from './components/Games.vue';

export default {
  name: 'app',
  components: {
      Games
  },
  data() {
    return{
      games: [
        {
          id: 1,
          title: "Astroneer",
          completed: false
        },        {
          id: 2,
          title: "Firewatch",
          completed: true
        },        {
          id: 3,
          title: "Stardew",
          completed: false
        }
      ]
    }
  },
  methods: {
    deleteGame(id){
      this.games = this.games.filter(game => game.id !== id);
    }
  }


}
</script>

<style>
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body{
    font-family: Arial;
    line-height: 1.4;
  }
</style>
