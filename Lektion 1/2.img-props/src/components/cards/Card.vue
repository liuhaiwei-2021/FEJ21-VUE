<template>
  <div class="card">
    <img :src="imgURL" class="card-img-top" alt="...">
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-text">{{ body }}</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
    
  </div>
</template>

<script>
export default {
  // data() {
  //   return {
  //     title: 'hej hej'
  //   }
  // }
  props: ['title', 'body', 'imgURL']
  // props: {
  //   title: {
  //     type: String,
  //     required: false,
  //     default: 'En standard text'
  //   },
  //   body: {
  //     type: String,
  //     required: false,
  //     default: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sapiente, officiis?'
  //   },
  //   imgURL: {
  //     type: String,
  //     required: false,
  //     default: '...'
  //   }
  // }
}
</script>

<style>

</style>