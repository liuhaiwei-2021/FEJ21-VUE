<template>
  <nav class="navbar navbar-light bg-light shadow mb-4">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="../assets/logo.png" alt="">
        {{ title }}
      </a>
    </div>
  </nav>
</template>

<script>
export default {
    props: {
        title: String
    }
};
</script>

<style>
.navbar-brand img {
    height: 50px;
    margin-right: 1rem;
}
</style>