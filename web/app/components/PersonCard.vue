<template>
  <div class="person-card">
    <div class="card-container">
      <img :src="`/images/people/${person.image}.png`" class="person" :alt="person.name" />
      <p class="hover-text">{{ person.text }}</p>
    </div>
    <div class="people-text">
      <h3>{{ person.name }}</h3>
      <p>{{ person.role }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  person: {
    type: Object
  }
})
</script>

<style scoped>
.person-card {
  display: flex;
  align-items: flex-end;
  gap: 30px;
}

.card-container {
  position: relative;
  width: fit-content;
  overflow: hidden;
}

.person {
  display: block;
  width: 35vw;
  max-width: 200px;
  height: auto;
  transition: transform 0.3s ease;
}

.hover-text {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;

  background: rgba(0, 0, 0, 0.7);
  color: white;
  margin: 0;
  padding: 20px;
  box-sizing: border-box;

  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;

  opacity: 0;
  transition: opacity 0.3s ease;

  font-size: 0.9rem;
}

.card-container:hover .hover-text {
  opacity: 1;
}

.card-container:hover .person {
  transform: scale(1.05);
}

.people-text {
  display: flex;
  flex-direction: column;
  gap: 5px;
}

.people-text h3 {
  margin: 0;
}

</style>