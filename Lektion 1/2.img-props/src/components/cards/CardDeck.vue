<template>
  <div class="card-deck">
    <Card :imgURL="imgOne" title='HEJ' body="alksdjopiwn ilkja sd" />
    <Card imgURL="/img/image2.jpg" title="HEJ2" body="jlaiwn dkinowkwqmpo q djkn aklqw" />
    <Card imgURL="https://images.unsplash.com/photo-1619382749984-02521fd9fc43?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2991&q=80" />
  </div>
</template>

<script>
import Card from './Card'
export default {
  components: {
    Card
  },
  data() {
    return {
      imgOne: require('@/assets/img/image1.jpg')
    }
  }
}
</script>

<style>

</style>