<template>
  <div id="home">
    <HeroSection />
    <FeatureSelection />
    <Footer />
  </div>
</template>

<script setup>
import HeroSection from './components/HeroSection.vue'
import FeatureSelection from './components/FeatureSelection.vue'
import Footer from './components/Footer.vue'
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}
</style>