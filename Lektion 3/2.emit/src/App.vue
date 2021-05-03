<template>
  <div class="container mt-5">
    <div class="row row-cols-2 g-4">
      <Display :name="name" :age="age" :email="email" />
      <Update :name="name" :age="age" :email="email" @update-user="update" />
    </div>
  </div>
</template>

<script>
import Display from './components/Display'
import Update from './components/Update'

export default {
  name: 'App',
  components: {
    Display,
    Update
  },
  data() {
    return {
      name: 'Joakim',
      age: 34,
      email: 'joakim.wahlstrom@mail.com'
    }
  },
  methods: {
    update(newUser) {
      this.name = newUser.name
      this.age = newUser.age
      this.email = newUser.email
    }
  }
}
</script>

<style>

</style>
