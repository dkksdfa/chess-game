<template>
  <div class="piece">
    <img :src="require(`../assets/${dataInt}.png`)"
    draggable=true @dragstart="dragStart" @click="ab">
  </div>
</template>

<script>

export default {
  name: 'ChessPiece',
  props: {
    dataInt: Number
  },
  methods: {
    ab () {
      console.log('클릭')
    },
    dragStart () {
      console.log('드래그')
    }
  }
}
</script>

<style scoped>
img {
  width: 50px;
  cursor: move;
}
</style>
