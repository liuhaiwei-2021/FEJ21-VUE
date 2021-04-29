<template>
  <div>
    <Navbar />
    <div class="container">
      <!-- <Methods /> -->
      <!-- <Events /> -->
      <!-- <FormInputs /> -->
      <Computed />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
// import Methods from './components/Methods.vue'
// import Events from './components/Events.vue'
// import FormInputs from './components/FormInputs'
import Computed from './components/Computed'

export default {
  name: 'App',
  components: {
    Navbar,
    // Methods,
    // Events,
    // FormInputs,
    Computed
  },

}
</script>

<style>

</style>
