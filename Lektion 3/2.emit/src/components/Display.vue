<template>
  <div class="col">
      <div class="card h-100">
        <div class="card-header bg-primary text-white py-4 text-center">
          <h2>{{ name }}</h2>
          <p>Age: {{ age }}</p>
        </div>
        <div class="card-body text-center">
          <p>Email: {{ email }}</p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  props: ['name', 'age', 'email']
}
</script>

<style>

</style>