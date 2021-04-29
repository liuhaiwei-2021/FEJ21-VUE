<template>
  <div>
    <Navbar />
    <CardGrid />

    <jumbotron title="Reusable Component" lead="Så här kan man återanvända en komponent" button="Läs mer om Vue här..." href="https://cli.vuejs.org" />
    <jumbotron title="Compoent 2" lead="Så här kan man återanvända en komponent" button="Läs mer om Vue här..." href="https://cli.vuejs.org" />
  </div>
</template>

<script>
import Navbar from './components/Navbar'
import Jumbotron from './components/Jumbotron'
import CardGrid from './components/CardGrid'

export default {
  name: 'App',
  components: {
    Navbar,
    Jumbotron,
    CardGrid
  }
}
</script>

<style>
.btn-primary {
  background-color: #41b883;
  border-color: #41b883;
}
.btn-primary:hover {
  background-color: #35495e;
  border-color: #35495e;
}
</style>
