<template>
  <div class="card">
      <h3>{{ user.name }}</h3>
      <p>{{ user.age }}</p>
    </div>
</template>

<script>
export default {
  props: ['user']
}
</script>

<style>

</style>