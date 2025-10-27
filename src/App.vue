<script setup>
import Header from './components/Header.vue'
import Content from './body/Content.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div id="app">
    <Header />
    <Content />
    <Footer />
  </div>
</template>

<style>
html, body {
  margin: 0;
  padding: 0;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: #1e1e1e;
}

#app > *:not(:first-child):not(:last-child) {
  flex: 1;
}
</style>
