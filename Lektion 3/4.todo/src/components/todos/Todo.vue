<template>
  <div>
    <div class="d-flex justify-content-between align-items-center border p-2 bg-white mb-1">
      <h3 :class="{done: todo.completed}" @click="toggle" >{{ todo.title }}</h3>
      <button class="btn btn-danger" @click="deleteTodo">X</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ['todo'],
  methods: {
    toggle() {
      this.todo.completed = !this.todo.completed
      this.$emit('toggle-completed', this.todo)
    },
    deleteTodo() {
      if(this.todo.completed)
        this.$emit('delete-todo', this.todo.id)
      else
        alert('du måste vara klar med en sak för att kunna ta bort den')
    }
  }
}
</script>

<style scoped>
  .done {
    text-decoration: line-through;
    color: #bbb;
  }
  h3 {
    cursor: pointer;
    user-select: none;
  }
</style>