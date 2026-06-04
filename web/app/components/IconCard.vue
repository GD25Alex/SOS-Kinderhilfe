<template>
  <div class="card-wrapper">
    <div class="circle">
      <img :src="`/images/symbols/${icon}.png`" class="icon" alt="Symbol" />
    </div>
    <p class="title" v-html="title" />
  </div>
</template>

<script setup>
defineProps({
  icon: {
    type: String,
    default: "handshake"
  },
  title: {
    type: String,
    default: "Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden"
  }
});
</script>

<style scoped>
.card-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 7px;
}

.circle {
  position: relative;
  background-color: var(--lightblue);
  width: 140px;
  height: 140px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 10px;

  transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.circle:hover {
  transform: scale(0.9);
}

.icon {
  width: 100px;
  height: auto;
}

.title {
  width: 260px;
  text-align: center;
}
</style>