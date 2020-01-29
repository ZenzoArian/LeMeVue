<template>
  <div id="app">
    <Header />
    <Games v-bind:games="games" v-on:del-game="deleteGame" />
  </div>
</template>

<script>
  import Header from './components/layout/Header';
  import Games from './components/Games.vue';

export default {
  name: 'app',
  components: {
    Header,
      Games
  },
  data() {
    return{
      games: [
        {
          id: 1,
          title: "Astroneer",
          description: "In this space sandbox adventure, players can work together to build custom bases above or below ground, create vehicles to explore a vast solar system, and use terrain to create anything they can imagine. A player’s creativity and ingenuity are the key to thriving on exciting planetary adventures!",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-ASTRONEER.png",
          completed: false
        },{
          id: 2,
          title: "Firewatch",
          description: "The year is 1989. You are a man named Henry who has retreated from his messy life to work as a fire lookout in the Wyoming wilderness. Perched high atop a mountain, it’s your job to look for smoke and keep the wilderness safe. An especially hot, dry summer has everyone on edge. Your supervisor Delilah is available to you at all times over a small, handheld radio—your only contact with the world you've left behind. But when something strange draws you out of your lookout tower and into the forest, you’ll explore a wild and unknown environment, facing questions and making choices that can build or destroy the only meaningful relationship you have.",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-firewatch.png",
          completed: false
        },{
          id: 3,
          title: "RocketLeague",
          description: "Rocket League is a high-powered hybrid of arcade-style soccer and vehicular mayhem with easy-to-understand controls and fluid, physics-driven competition. Rocket League includes casual and competitive Online Matches, a fully-featured offline Season Mode, special “Mutators” that let you change the rules entirely, hockey and basketball-inspired Extra Modes, and more than 500 trillion possible cosmetic customization combinations.",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-rocket-league.png",
          completed: false
        },{
          id: 4,
          title: "CounterStrike",
          description: "Counter-Strike took the gaming industry by surprise when the unlikely MOD became the most played online PC action game in the world almost immediately after its release in August 1999,\" said Doug Lombardi at Valve. \"For the past 12 years, it has continued to be one of the most-played games in the world, headline competitive gaming tournaments and selling over 25 million units worldwide across the franchise. CS: GO promises to expand on CS' award-winning gameplay and deliver it to gamers on the PC as well as the next gen consoles and the Mac.\"",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-csgo.png",
          completed: false
        },{
          id: 5,
          title: "Rainbowsix siege",
          description: "Master the art of destruction and gadgetry in Tom Clancy’s Rainbow Six Siege. Face intense close quarters combat, high lethality, tactical decision making, team play and explosive action within every moment. Experience a new era of fierce firefights and expert strategy born from the rich legacy of past Tom Clancy's Rainbow Six games.\n",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-rainbow.png",
          completed: false
        },{
          id: 6,
          title: "Apex legends",
          description: "A remote cluster of planets on the fringes of the Frontier, the Outlands are untouched by war and teeming with resources and opportunity. But life is cheap here, and danger lurks around every corner. Its pioneers, explorers, and outlaws used to spend their lives locked in an endless power struggle – now, they settle their differences in the Apex Games, a bloodsport where Legends from all corners of the Frontier compete for money, fame, and glory.",
          image: "http://25453.hosts2.ma-cloud.nl/bewijzenmap/periode3.3/FRO/CD%20covers/image/cover-apex.png",
          completed: false
        },
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
