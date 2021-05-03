<template>
  <div>
    <div v-for="todo in todos" :key="todo.id">
      <Todo /> 
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