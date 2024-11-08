<script setup>
// import SquareDiv from '../components/SquareDiv.vue'
import PillDiv from '../components/PillDiv.vue'
</script>

<template>
  <main>
    <PillDiv v-for="n in 400" :key="n" class="square" />
  </main>
</template>

<style scoped>
main {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  width: 100vw;
  height: 100vh;
  background-color: #7f7d5531;
  gap: 10px;
  overflow-y: hidden;
  overflow-x: hidden;
  font-family: 'Poppins';
  /* font-style: italic; */

  /* border-radius: 6px; */

  box-shadow:
    0 4px 12px rgba(0, 0, 0, 0.321),
    0 2px 4px rgba(0, 0, 0, 0.263);
}

main::before {
  content: '';

  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  /* background-image: url('../assets/bluebg.png'); */
  background-image: url('../assets/wp.png');

  /* background: linear-gradient(90deg, #F8D5C6, #2E537C); */
  background: linear-gradient(to bottom, #f4f8fb, #e1ecf4, #cfe0ed, #bcd4e6, #a9c8df);

  background-size: cover;
  background-position: center;
  opacity: 0.45;
  z-index: -1;
}
</style>
