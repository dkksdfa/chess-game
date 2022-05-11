<template>
  <div class="board">
    <div v-for="rank in boardList" :key="rank.id" class="rank">
      <div v-for="file in rank" :key="file.id" class="file">
        <ChessPiece :dataInt="file" v-if="file != 0"></ChessPiece>
      </div>
    </div>
  </div>
</template>

<script>
import ChessPiece from './ChessPiece.vue'
export default {
  name: 'ChessBoard',
  components: {
    ChessPiece
  },
  props: {
    boardList: Array
  },
  data () {
    return {
      board: this.boardList
    }
  }
}
</script>

<style scoped>
  .file {
    display: inline-block;
    width: 50px;
    height: 50px;
    border: 1px solid black;
  }
</style>
