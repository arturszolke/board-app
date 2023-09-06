<script lang="ts">
import BoardStatus from './components/BoardStatus.vue'

export default {
  name: 'App',
  components: {
    BoardStatus
  },
  data() {
    return {
      status: [
        { id: 1, name: 'Todo', tasks: [] },
        { id: 2, name: 'In Progress', tasks: [] },
        { id: 3, name: 'Done', tasks: [] },
        { id: 4, name: 'Test', tasks: [] },
      ]
    }
  },
}

</script>

<template>
  <div v-for="(state, id) in status" :key="id" class="app">
    <BoardStatus :status="state" />
  </div>
</template>

<style scoped>
.app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
