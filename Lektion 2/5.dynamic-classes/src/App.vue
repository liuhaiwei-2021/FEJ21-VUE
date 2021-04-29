<template>
  <div id="app">
    <Navbar title="Vue Dynamic classes" />
    <div class="container">
      <!-- <Example1 /> -->
      <!-- <Example2 /> -->
      <Example2Extended />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
// import Example1 from './components/Example1'
// import Example2 from './components/Example2'
import Example2Extended from './components/Example2Extended'

export default {
  name: 'App',
  components: {
    Navbar,
    // Example1,
    // Example2,
    Example2Extended
  }
}
</script>

<style>

</style>
