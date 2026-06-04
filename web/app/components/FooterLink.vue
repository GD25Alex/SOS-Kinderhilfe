<template>
  <div>
    <p class="navigation" :class="[size]">
      <slot />
    </p>
  </div>
</template>

<script setup>
defineProps({
  size: {
    type: String,
    default: 'medium',
    validator: (value) => ['small', 'medium', 'large'].includes(value)
  }
})
</script>

<style scoped>
.navigation {
  font-weight: 200;
  color: gray;
  padding: 3px;
  cursor: pointer;
  transition: font-size 0.2s ease;
}

.small {
  font-size: 14px;
}

.medium {
  font-size: 18px;
}

.large {
  font-size: 26px;
}

.navigation:hover {
  color: var(--blue);
}

.active {
  background-color: var(--black);
  color: white;
}
</style>