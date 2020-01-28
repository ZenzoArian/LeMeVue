<template>
  <div id="app">

  </div>
</template>

<script>

export default {
  name: 'app',
  components: {

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
