<template>
  <div class="board">
    <div v-for="rank in boardList" :key="rank.id" class="rank">
      <div v-for="file in rank" :key="file.id" class="file">
        {{file}}
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'ChessBoard',
  components: {
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
  }
</style>
