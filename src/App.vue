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
                {
                    id: 1, name: 'Todo', tasks: [
                        {
                            id: 1,
                            title: 'Task 1',
                            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod, nisl eget tempor aliquam, nunc libero ultricies nunc, quis aliquet nisl nunc eu nisl. Sed vitae nisl eget nisl aliquet aliquam. Sed vitae nisl eget nisl aliquet aliquam.',
                        },
                        {
                            id: 2,
                            title: 'Task 2',
                            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod, nisl eget tempor aliquam, nunc libero ultricies nunc, quis aliquet nisl nunc eu nisl. Sed vitae nisl eget nisl aliquet aliquam. Sed vitae nisl eget nisl aliquet aliquam.',
                        }
                    ]
                },
                { id: 2, name: 'In Progress', tasks: [] },
                {
                    id: 3, name: 'Done', tasks: [
                        {
                            id: 1,
                            title: 'Task 1',
                            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec euismod, nisl eget tempor aliquam, nunc libero ultricies nunc, quis aliquet nisl nunc eu nisl. Sed vitae nisl eget nisl aliquet aliquam. Sed vitae nisl eget nisl aliquet aliquam.',
                        },
                    ]
                },
                { id: 4, name: 'Test', tasks: [] },
            ]
        }
    },
}

</script>

<template>
    <button @click="console.log(status)">status</button>
    <div class="app m-0">
        <div class="row">
            <div class="col p-0" v-for="(state, id) in status" :key="id">
                <BoardStatus :status="state" />
            </div>
        </div>
    </div>
</template>

<style scoped>
.app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: black;
    background-color: white;
    height: 100vh;
}
</style>
