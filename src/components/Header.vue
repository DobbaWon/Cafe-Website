<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const isScrolled = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50 // adjust threshold as needed
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <div :class="['header', { scrolled: isScrolled }]">
    <h1>Cafe Name</h1>

    <div class="header-spacer">
      <a href="#"><h2>Home</h2></a>
      <a href="#"><h2>Menu</h2></a>
      <a href="#"><h2>Contact</h2></a>
    </div>
  </div>
</template>

<style scoped>
.header {
  position: fixed;
  z-index: 100;
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  background-color: rgba(42, 42, 42, 1);
  transition: background-color 0.3s ease, backdrop-filter 0.3s ease, opacity 0.3s ease;
  height: 12vh;
  padding: 0 2rem;
  opacity: 0.6;
}

/* When user scrolls down */
.header.scrolled {
  background-color: rgba(42, 42, 42, 0.8);
  backdrop-filter: blur(6px);
  opacity: 0.8; /* reduce opacity */
}

.header h1 {
  color: white;
  font-size: 2.2rem;
  margin-left: 2rem;
}

.header-spacer {
  display: flex;
  gap: 2rem;
  margin-right: 5rem;
}

.header-spacer a {
  text-decoration: none;
}

.header-spacer h2 {
  margin: 0;
  font-size: 1.2rem;
  color: white;
  transition: color 0.2s ease;
}

.header-spacer h2:hover {
  color: #ccc;
}
</style>
