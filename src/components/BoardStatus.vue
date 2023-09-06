<script lang="ts">
import Draggable from 'vuedraggable'
import BoardTask from './BoardTask.vue'

export default {
    name: 'BoardStatus',
    props: ['status'],
    components: {
        Draggable,
        BoardTask
    },
}
</script>

<template>
    <div class="wrapper m-4 rounded">
        <div class="boardStatus rounded">
            <div class="fw-bolder statusName rounded-top">
                <h2 class="p-3 text-start">{{ status.name }} <span class="fs-4 text-muted">{{ status.tasks.length }}</span>
                </h2>
            </div>
            <div>
                <Draggable class="draggable" ghost-class="ghost" drag-class="dragClass" group="tasks"
                    fallback-class="fallbackStyleClass" :force-fallback="true" :animation="200" :list="status.tasks"
                    item-key="index">
                    <template #item="{ element: task }">
                        <BoardTask :task="task" />
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

.fallbackStyleClass {
    opacity: 1 !important;
}

.ghost {
    visibility: hidden;
}

.ghost>div {
    visibility: hidden !important;
}
</style>