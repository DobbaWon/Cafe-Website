<script setup>
import leftImage from '@/assets/gallery1.png'
import rightImage from '@/assets/gallery2.jpeg'
</script>

<template>
  <section class="gallery">
    <div class="top-left-text">
      <p>
        <span class="mission-title">Our mission</span> at the Cafe Name is to bring fresh, fine dining to the people of City. To compliment the surrounding businesses by providing delicious food, fine wines and cocktails.
      </p>
      <p>
        Sourcing as many of our ingredients and produce as we can from local suppliers. Employing local staff. We want to be in the heart of the local community.
      </p>
      <p>
        The Cafe Name is a family run business. With large ‘chain’ experience, we are passionate about food, flavour and fun.
      </p>
    </div>

    <div class="bottom-left-image">
      <img :src="leftImage" alt="Bottom-left image" />
    </div>

    <div class="right-image">
      <img :src="rightImage" alt="Right-side image" />
    </div>
  </section>
</template>

<style scoped>
.gallery {
  display: grid;
  grid-template-columns: 1fr 1fr; 
  grid-template-rows: 1fr 1fr; 
  gap: 2rem;
  padding: 5vw;
  height: 140vh;
  background-color: rgb(242, 231, 231);
  box-sizing: border-box;
}

/* Top-left text */
.top-left-text {
  grid-column: 1;
  grid-row: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: 0 2.5vw;
}

.mission-title {
  font-weight: bold;
  margin-bottom: 1rem;
  font-size: 2rem;
  color: #dd5903
}

.top-left-text p {
  margin-bottom: 1rem;
  line-height: 1.5;
  color: #333;
}

/* Bottom-left image */
.bottom-left-image {
  grid-column: 1;
  grid-row: 2;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}

/* Right image spans both rows */
.right-image {
  grid-column: 2;
  grid-row: 1 / span 2;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 2.5vw;
}

.right-image img {
  width: 100%;
  height: 100%;
}
</style>
