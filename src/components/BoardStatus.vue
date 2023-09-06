<script lang="ts">
export default {
    name: 'BoardStatus',
    props: ['status']
}
</script>

<template>
    <div class="wrapper">
        <div class="boardStatus">
            <div>
                {{ status.name }}
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
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid white;
    width: 200px;
    height: 200px;
    margin: 10px;
}
</style>