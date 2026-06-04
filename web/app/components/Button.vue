<template>
  <div class="button-wrapper" :class="{ 'is-outlined': outlined }">
    <p class="text">
      <slot />
    </p>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  outlined: {
    type: Boolean,
    default: false
  },
  color: {
    type: String,
    default: 'orange',
    validator: (value) => ['orange', 'blue'].includes(value)
  }
})

const buttonColor = computed(() => `var(--${props.color})`)
</script>

<style scoped>
.button-wrapper {
  --btn-color: v-bind(buttonColor);

  border-radius: 16px;
  border: 1px solid var(--btn-color);
  background-color: var(--btn-color);
  color: white;
  width: fit-content;
  padding: 5px 25px;
  transition: all 0.2s ease;
  cursor: pointer;
}

.button-wrapper.is-outlined {
  background-color: transparent;
  color: var(--btn-color);
}

.button-wrapper .text {
  font-size: 25px;
  font-weight: 400;
}
</style>