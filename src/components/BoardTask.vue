<script lang="ts">
export default {
    name: 'BoardTask',
    props: ['task'],
}
</script>

<template>
    <div class="drag bg-white rounded-2 m-2 p-2">
        <h4 class="text-start">
            {{ task.title }}
        </h4>
        <p class="text-start">
            {{ task.description }}
        </p>
    </div>
</template>

<style scoped>
.drag {
    cursor: grab;
}
</style>