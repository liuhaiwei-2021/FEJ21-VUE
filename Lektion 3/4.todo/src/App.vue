<template>
  <div class="bg-light">
    <Navbar />
    <AddTodo />

    <div class="container py-5">
      <TodosList :todos="todos" />
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
      todos: []
    }
  },
  methods: {
    async getTodos() {
      const res = await axios.get('http://localhost:3000/todos')
      this.todos = res.data
    }
  },
  created() {
    this.getTodos()
  }
}
</script>

<style>

</style>
