<template>
  <div class="stage-wrapper">
    <img :src="`/images/${image}.png`" alt="Stage Hintergrund" class="logo" :style="{ objectPosition: focusPoint }" />
    <div class="overlay"></div>
    <h1 class="stage-title" v-html="title"></h1>
    <div class="donation desktop-only-flex" @click="navigateTo('/spenden')">
      <p class="title">Deine Spende <br /> zählt!</p>
      <p class="action">Jetzt <br>Spenden!</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    default: 'Gemeinsam für <br> neue Perspektiven'
  },
  image: {
    type: String,
    default: 'image1'
  },
  focusPoint: {
    type: String,
    default: 'center center'
  }
})
</script>

<style scoped>
.stage-wrapper {
  position: relative;
  height: 45vh;
  width: 100%;
  overflow: hidden;
  display: flex;
}

.logo {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.2);
}

.stage-title {
  position: absolute;
  color: white;
  z-index: 1;
  background-color: var(--black);
  text-transform: uppercase;
  bottom: 30%;
  left: 18%;
  margin: 0;
  padding: 4px 0px;
  font-size: 2.8rem;
  font-weight: 700;
  line-height: 0.9;
}

.donation {
  position: absolute;
  z-index: 1;
  color: white;
  right: 20%;
  bottom: 20%;
  background-color: var(--orange);
  width: 140px;
  height: 140px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 10px;
  transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
  cursor: pointer;
}

.donation p {
  position: absolute;
  margin: 0;
  line-height: 0.8;
  font-weight: 900;
  font-size: 35px;
  text-transform: uppercase;
  transition: opacity 0.3s cubic-bezier(0.34, 1.56, 0.64, 1), transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.donation .title {
  opacity: 1;
  transform: scale(1);
}

.donation .action {
  opacity: 0;
  transform: scale(0.8);
}

.donation:hover {
  transform: scale(1.1);
}

.donation:hover .title {
  opacity: 0;
  transform: scale(0.8);
}

.donation:hover .action {
  opacity: 1;
  transform: scale(1.1);
}
</style>