<script lang="ts">
export default {
    name: 'BoardStatus',
    props: ['status']
}
</script>

<template>
    <div class="wrapper m-5 rounded">
        <div class="boardStatus rounded">
            <div class="fw-bolder statusName rounded-top">
                <h2 class="py-3">{{ status.name }}</h2>
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
</style>