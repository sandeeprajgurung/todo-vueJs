<template>
  <div id="home">
   
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import AddTodo from '../components/layouts/AddTodo.vue';

import Todos from '../components/Todos.vue';

export default {
  name: 'home',
  components: {
    AddTodo,
    Todos
  }, 
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Todo one',
          completed: false
        },
        {
          id: 2,
          title: 'Todo two',
          completed: false
        },
        {
          id: 3,
          title: 'Todo three',
          completed: true
        }
      ]
    }
  },
  methods: {
    deleteTodo(id) {
        this.todos = this.todos.filter(todo => todo.id !== id);
    },
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];
    }
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
  div {
      background-color: #f2f2f2;
  }
</style>
