<template>
  <div class="c-container">
    <div v-for="(item, index) in images" :key="index" class="image-container">
      <img :src="`/images/${item.image}.png`" :alt="item.title" class="image" />
    </div>
  </div>
</template>

<script setup>

const props = defineProps({
  images: {
    type: Array,
    default: () => [
      { "title": "Image1", "image": "image6" },
      { "title": "Image2", "image": "image7" }
    ]
  },
  cols: {
    type: Number,
    default: 2,
  },
  fit: {
    type: String,
    default: 'cover',
    validator: (value) => ['cover', 'contain', 'fill'].includes(value)
  }
})
</script>

<style scoped>
.c-container {
  width: 100%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(v-bind(cols), 1fr);

  gap: 20px;
  padding: 20px 0px;
}

.image-container {
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.image {
  width: 100%;
  max-height: 80vh;
  object-fit: v-bind(fit);
}
</style>