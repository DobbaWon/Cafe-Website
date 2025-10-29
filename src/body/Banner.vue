<script setup>
</script>

<template>
  <div class="banner">
    <h2>A warm welcome to</h2>
    <h1>Cafe Name</h1>
  </div>
</template>

<style scoped>
.banner {
  background-image: url('path/to/your/image.jpg');
  background-size: cover;
  background-position: center;
  height: 100vh;
  width: 100vw;
  object-fit: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
}
.banner h1 {
  font-size: 4rem;
  margin: 0;
}
.banner h2 {
  font-size: 2rem;
  margin: 0 0 1rem 0;
}
</style>