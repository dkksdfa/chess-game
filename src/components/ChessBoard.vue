<template>
  <div class="board">
    <div v-for="(rank, i_index) in boardList" :key="rank.id" class="rank">
      <div v-for="(file, j_index) in rank" :key="file.id" class="file">
        <ChessPiece :propInt="file" @emitSelect="setSelect" :propRed="redCal(i_index, j_index)"></ChessPiece>
      </div>
    </div>
  </div>
</template>

<script>
import ChessPiece from './ChessPiece.vue'
import {} from '../js/chess.js'
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
      board: this.boardList,
      select: 0
    }
  },
  watch: {
    select (data, oldData) {
      switch (data) {
        case 1:
        case 7:
          break
      }
    }
  },
  methods: {
    setSelect (value) {
      this.select = value
    },
    redCal (i, j) {
      if (this.board[i][j] > 0) return 'red'
      return ''
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
