<template>
  <div v-if="users.length">
    <User v-for="user in users" :key="user.id" :user="user" />
  </div>
  <div v-else>
    <h3>No users registered</h3>
  </div>
</template>

<script>
import User from './User'
export default {
  props: ['users'],
  components: {
    User
  }
}
</script>

<style scoped>
  .card {
    border: 1px solid #333;
    margin-bottom: 2rem;
    padding: 1rem;
    border-radius: 1rem;
  }
</style>