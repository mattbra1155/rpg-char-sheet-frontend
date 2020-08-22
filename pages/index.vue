<template>
    <main class="main container">
        <h1 class="header"></h1>
        <button @click="getFirstToDo">Click</button>
        <p v-if="toDo">{{ toDo }}</p>
    </main>
</template>

<script>
import Axios from 'axios'
export default {
    async asyncData() {
        const { data } = await Axios.get(
            'https://jsonplaceholder.typicode.com/todos/'
        )

        return { name: data }
    },
    data() {
        return {
            name: '',
            toDo: '',
        }
    },
    methods: {
        async getFirstToDo() {
            const { data } = await Axios.get(
                'https://jsonplaceholder.typicode.com/todos/1'
            )
            console.log(data)
            this.toDo = data
        },
    },
}
</script>

<style lang="scss" scoped>
.container {
    margin: 10px;
}
</style>
