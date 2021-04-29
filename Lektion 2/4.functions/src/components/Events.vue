<template>
  <div class="mb-5">
        <h1 class="display-5">Events</h1>
      
        <div class="my-5">{{ amount }}</div>
      
        <div><button @click="add" class="btn btn-secondary mb-2">Click Event</button></div>
        <div><button @dblclick="add" class="btn btn-secondary mb-2">Double Click Event</button></div>
        <div><button @mouseover="add" class="btn btn-secondary mb-2">Mouseover Event</button></div>
      
  </div>
</template>

<script>
export default {
    data() {
        return {
            amount: 0
        }
    },
    methods: {
        add() {
            this.amount++
        }
    }
}
</script>

<style>

</style>