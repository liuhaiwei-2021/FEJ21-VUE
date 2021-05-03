<template>
  <footer>
    <h3>copyright 2021 {{ title }}</h3>
  </footer>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style scoped>
  footer {
    background: darkslateblue;
    color: #fff;
    padding: 2rem;
  }
</style>