<template>
  <div class="container">
      <div class="bg-dark text-light p-5 m-3 rounded">
          <h1 class="display-4">{{title}}</h1>
          <p class="lead">{{lead}}</p>
          <hr class="my-4">
          <a class="btn btn-primary" :href=href target="_blank">{{button}}</a>
      </div>
  </div>
</template>

<script>
export default {
    props: {
        title: String,
        lead: String,
        button: {
            type: String,
            default: 'Read More...'
        },
        href: String
    }
}
</script>

<style>

</style>