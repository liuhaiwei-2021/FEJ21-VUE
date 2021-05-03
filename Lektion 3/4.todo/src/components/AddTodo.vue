<template>
  <div class="border-bottom bg-white">
    <form class="py-5 container" @submit.prevent="addTodo">
      <div class="row">

        <div class="col-8">
          <div class="input-group mb-3">
            <input type="text" class="form-control" placeholder="Add todo..." v-model="title">
            <button class="btn btn-info">ADD</button>
          </div>
        </div>

        <div class="col-4">
          <select class="form-select">
            <option selected>Show all</option>
            <option value="false">Show Uncompleted</option>
            <option value="true">Show Completed</option>
          </select>
        </div>

      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: ''
    }
  }, 
  methods: {
    addTodo() {
      if(this.title !== '') {
        this.$emit('addTodo', this.title)
        this.title = ''
      } else {
        alert('skriv in nått')
      }
    }
  }
}
</script>

<style>

</style>