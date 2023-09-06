<script lang="ts">
import Draggable from 'vuedraggable'

export default {
    name: 'BoardStatus',
    props: ['status'],
    components: {
        Draggable
    },
}
</script>

<template>
    <div class="wrapper m-5 rounded">
        <div class="boardStatus rounded">
            <div class="fw-bolder statusName rounded-top">
                <h2 class="p-3 text-start">{{ status.name }} <span class="fs-4">{{ status.tasks.length }}</span></h2>
            </div>
            <!-- <div v-for="(task, id) in status.tasks" :key="id">
                {{ task.title }}
                {{ task.description }}
            </div> -->
            <div>
                <Draggable class="draggable" ghost-class="ghost" drag-class="dragClass" group="tasks"
                    fallback-class="fallbackStyleClass" :force-fallback="true" :animation="200" :list="status.tasks"
                    item-key="id">
                    <template #item="{ element: task }">
                        <div class="drag bg-white rounded-2 m-2 p-2">
                            <h4 class="text-start">
                                {{ task.title }}
                            </h4>
                            <p class="text-start">
                                {{ task.description }}
                            </p>
                        </div>
                    </template>
                </Draggable>
            </div>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
}

.boardStatus {
    width: 100%;
    min-height: 800px;
    background-color: #dbdbdb;

}

.statusName {
    background-color: #3b3b3b;
    color: #EEE5E9;
}

.draggable {
    min-height: 500px;
}

.drag {
    cursor: grab;
}

.fallbackStyleClass {
    opacity: 0.75 !important;
}

.ghost {
    visibility: hidden;
}

.ghost>div {
    visibility: hidden !important;
}
</style>