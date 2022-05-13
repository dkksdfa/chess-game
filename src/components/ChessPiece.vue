<template>
  <div :class="propRed" v-if="propInt != 0">
    <img :src="require(`../assets/${propInt}.png`)"
    draggable=true @dragstart="emit()" @click="emit()">
  </div>
  <div :class="propRed" v-else>
  </div>
</template>

<script>

export default {
  name: 'ChessPiece',
  emits: 'dataEmit',
  props: {
    propInt: Number,
    propRed: String
  },
  methods: {
    emit () {
      this.$emit('emitSelect', this.propInt)
    }
  }
}
</script>

<style scoped>
img {
  width: 50px;
  cursor: move;
}
.red {
  border: 1px solid red;
}
</style>
