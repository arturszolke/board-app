<script lang="ts">
export default {
    name: 'BoardStatus',
    props: ['status']
}
</script>

<template>
    <div class="wrapper m-5 rounded-2">
        <div class="boardStatus">
            <div class="">
                <h2>{{ status.name }}</h2>
            </div>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid black;
}

.boardStatus {
    width: 200px;
    min-height: 600px;
}
</style>