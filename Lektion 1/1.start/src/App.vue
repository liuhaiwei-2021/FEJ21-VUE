<template>
  <div>
    <appNavbar />
    <Hero />
    <Testimonials />
    <Pricing />
    <Features />
    <app-footer />
  </div>
</template>

<script>
import navbar from './components/navigation/Navbar'
import Footer from './components/navigation/Footer'
import Hero from './components/Hero'
import Testimonials from './components/testimonials/Testimonials'
import Features from './components/Features'
import Pricing from './components/Pricing'

export default {
  name: 'App',
  components: {
    AppNavbar: navbar,
    appFooter: Footer,
    Hero,
    Testimonials,
    Features,
    Pricing
  }
}
</script>

<style>

</style>
