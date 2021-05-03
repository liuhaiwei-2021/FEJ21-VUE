<template>
  <div>
    <transition-group name="fade-slide">
      <div v-for="todo in todos" :key="todo.id">
        <Todo v-if="value === ''" :todo="todo" @delete-todo="$emit('delete-todo', todo.id)" @toggle-completed="$emit('toggle-completed', todo)"/> 
        <Todo v-else-if="todo.completed === value" :todo="todo" @delete-todo="$emit('delete-todo', todo.id)" @toggle-completed="$emit('toggle-completed', todo)"/> 
      </div>
    </transition-group>
  </div>
</template>

<script>
import Todo from './Todo'
export default {
  props: ['todos', 'value'],
  components: {
    Todo
  }
}
</script>

<style>

.fade-slide-enter-active, .fade-slide-leave-active {
  transition: all 0.5s ease;
}
.fade-slide-enter {
  opacity: 0;
  transform: translateX(-50px);
}
.fade-slide-leave-to {
  opacity: 0;
  transform: translateX(50px);
}

</style>