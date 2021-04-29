<template>
  <div class="card">
      <img :src=imgSrc class="card-img-top" :alt=imgAlt>
      <div class="card-body">
        <h5 class="card-title">{{title}}</h5>
        <p class="card-text">{{text}}</p>
      </div>
    </div>
</template>

<script>
export default {
    props: {
        imgSrc: String,
        imgAlt: {
            type: String,
            default: ""
        },
        title: String,
        text: String
    }
}
</script>

<style>
.card-img-top {
    height: auto;
    width: 150px;
}
</style>