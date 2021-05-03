<template>
  <div class="bg-light">
    <Navbar />
    <AddTodo @addTodo="add" @sort="sortTodos" />

    <div class="container py-5">
      <TodosList :value="sort" :todos="todos" @delete-todo="deleteTodo" @toggle-completed="toggle" />
    </div>

  </div>
</template>

<script>
import Navbar from './components/Navbar'
import AddTodo from './components/AddTodo'
import TodosList from './components/todos/TodosList'

import axios from 'axios'

export default {
  name: 'App',
  components: {
    Navbar,
    AddTodo,
    TodosList
  },
  data() {
    return {
      todos: [],
      sort: ''
    }
  },
  methods: {
    sortTodos(val) {
      switch(val) {
        case 'false':
          this.sort = false
          break
        case 'true':
          this.sort = true
          break
        default:
          this.sort = ''
      }
    },
    async getTodos() {
      const res = await axios.get('http://localhost:3000/todos')
      this.todos = res.data
    },
    add(title) {
      let todo = {
        title,
        completed: false
      }

      axios.post('http://localhost:3000/todos', todo)
      .then(() => {
        this.getTodos()
      })
    },
    deleteTodo(id) {
      axios.delete('http://localhost:3000/todos/' + id)
      .then(() => {
        this.getTodos()
      })
    },
    toggle(todo) {
      axios.put('http://localhost:3000/todos/' + todo.id, todo)
    }
  },
  created() {
    this.getTodos()
  }
}
</script>

<style>

</style>
