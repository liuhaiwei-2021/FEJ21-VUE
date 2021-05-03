<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <Todo :todo="todo" @delete-todo="$emit('delete-todo', todo.id)" @toggle-completed="$emit('toggle-completed', todo)"/> 
    </div>
  </div>
</template>

<script>
import Todo from './Todo'
export default {
  props: ['todos'],
  components: {
    Todo
  }
}
</script>

<style>

</style>