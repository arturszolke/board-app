<script setup lang="ts">
import BoardStatus from './components/BoardStatus.vue'

export default {
  name: 'App',
  components: {
    BoardStatus
  }
}
</script>

<template>
  <div id="app">
    <BoardStatus />
  </div>
</template>

<style scoped></style>
