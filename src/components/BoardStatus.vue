<script lang="ts">
export default {
    name: 'BoardStatus',
    props: ['status']
}
</script>

<template>
    <div class="wrapper">
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
}

.boardStatus {
    border: 1px solid black;
    width: 200px;
    height: 200px;
    margin: 10px;
}
</style>