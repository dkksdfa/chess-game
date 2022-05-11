<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <ChessBoard v-bind:boardList="board"/>
</template>

<script>
import ChessBoard from './components/ChessBoard.vue'

export default {
  name: 'App',
  components: {
    ChessBoard
  },
  data () {
    return {
      board: [
        [10, 8, 9, 11, 12, 9, 8, 10],
        [7, 7, 7, 7, 7, 7, 7, 7],
        [0, 0, 0, 0, 0, 0, 0, 0],
        [0, 0, 0, 0, 0, 0, 0, 0],
        [1, 1, 1, 1, 1, 1, 1, 1],
        [4, 2, 3, 5, 6, 3, 2, 4]
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
