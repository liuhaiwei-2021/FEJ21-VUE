<template>
  <div>
    <form @submit.prevent="handleSubmit">
      <input type="text" v-model="name">
      <input type="number" v-model="age">
      <button>add</button>
    </form>
    <Names :names="names" />
    <Loop :names="names" />
    <Users :users="users" />
    <Objects :users="users" />
  </div>
</template>

<script>
import Names from './components/Names'
import Loop from './components/Loop'
import Users from './components/Users'
import Objects from './components/Objects'

export default {
  name: 'App',
  components: {
    Names,
    Loop,
    Users,
    Objects,
  },
  data() {
    return {
      names: ['Joakim', 'Jeanette', 'Hans', 'Tommy', 'Haitem', 'John'],
      users: [
        { id: 1, name: 'Joakim', age: 34 },
        { id: 2, name: 'Jeanette', age: 33 },
        { id: 3, name: 'Hans', age: 36 }
      ],
      name: '',
      age: 30
    }
  },
  methods: {
    handleSubmit() {
      this.users.push({
        id: Date.now(),
        name: this.name,
        age: this.age
      })
    }
  }
}
</script>

<style>

</style>
