<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <!-- <h3>{{todo.title}}</h3> -->
            <TodoItems v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItems from './TodoItems.vue';

export default {
    name: 'Todos',
    components: {
        TodoItems
    },
    props: ['todos']
}
</script>

<style scoped>

</style>