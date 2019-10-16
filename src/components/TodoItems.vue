<template>
    <div class="todo-items-wrapper" v-bind:class="{'is-complete':todo.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{todo.title}}
            <button @click="$emit('delete-todo', todo.id)" class="button">Delete</button>
        </p>
        <!-- <p>{{todo.completed}}</p> -->
    </div>
</template>

<script>
export default {
    name: "TodoItems",
    props: ["todo"],
    methods: {
        markComplete() {
            // console.log('123');
            this.todo.completed = !this.todo.completed;
        }
    }
}
</script>

<style scoped>
    p {
        font-size: 20px;
    }
    .todo-items-wrapper {
        background: rgb(111, 189, 172);
        padding: 1px;
        border-bottom: 1px solid #ccc;
    }
    .is-complete {
        text-decoration: line-through;
    }

    .button {
        display: inline-block;
        padding: 15px 15px;
        font-size: 15px;
        cursor: pointer;
        text-align: center;
        text-decoration: none;
        outline: none;
        color: #fff;
        background-color: #4CAF50;
        border: none;
        border-radius: 15px;
        box-shadow: 0 9px #999;
        margin-bottom: 10px;
        margin-left: 90px;
    }
    .button:hover {background-color: #3e8e41}
    .button:active {
        background-color: #3e8e41;
        box-shadow: 0 5px #666;
        transform: translateY(4px);
    }
</style>