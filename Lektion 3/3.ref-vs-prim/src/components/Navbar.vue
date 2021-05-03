<template>
  <nav>
    <h1 @click="$emit('changeTitle', 'Hej')">{{ title }}</h1>
  </nav>
</template>

<script>
export default {
  props: ['title']
}
</script>

<style scoped>
  nav {
    background: darkslateblue;
    padding: 2rem;
    color: #fff;
  }
</style>