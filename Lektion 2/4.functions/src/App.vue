<template>
  <div>
    <Navbar />
    <div class="container">
      <!-- <Methods /> -->
      <!-- <Events /> -->
      <FormInputs />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
// import Methods from './components/Methods.vue'
// import Events from './components/Events.vue'
import FormInputs from './components/FormInputs'

export default {
  name: 'App',
  components: {
    Navbar,
    // Methods,
    // Events,
    FormInputs
  },

}
</script>

<style>

</style>
