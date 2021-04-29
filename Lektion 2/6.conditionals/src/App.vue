<template>
  <div>
      <AdminNavbar v-if="checkAdminRole" />
      <Navbar title="Vue Conditionals" :signedIn="signedIn" />
      <div class="container mt-5">
        <Table />
      </div>
      
      
  </div>
</template>

<script>
import AdminNavbar from './components/AdminNavbar'
import Navbar from './components/Navbar'
import Table from './components/Table'

export default {
  name: 'App',
  components: {
    AdminNavbar,
    Navbar,
    Table
  },
  data() {
    return {
      signedIn: true,
      isAdmin: false
    }
  },
  computed: {
    checkAdminRole() {
      if(this.signedIn && this.isAdmin)
        return true
      else
        return false
    }
  }
}
</script>

<style>

</style>
