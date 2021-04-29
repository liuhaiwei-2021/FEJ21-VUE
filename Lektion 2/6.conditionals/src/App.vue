<template>
  <div>
      <AdminNavbar v-if="checkAdminRole" />
      <Navbar title="Vue Conditionals" :signedIn="signedIn" />
  </div>
</template>

<script>
import AdminNavbar from './components/AdminNavbar'
import Navbar from './components/Navbar'

export default {
  name: 'App',
  components: {
    AdminNavbar,
    Navbar
  },
  data() {
    return {
      signedIn: true,
      isAdmin: true
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
