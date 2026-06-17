<template>
  <div class="link-container" :class="[{ 'highlight-content': highlight }]">
    <p><strong>{{ title }}</strong></p>
    <div class="link-content">
      <img v-if="highlight" src="/images/symbols/arrow.png" class="arrow" />

      <p class="navigation" :class="[size, { 'active': active, 'highlight': highlight }]">
        <slot />
      </p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  size: {
    type: String,
    default: 'medium',
    validator: (value) => ['small', 'medium', 'large'].includes(value)
  },
  active: {
    type: Boolean,
    default: false
  },
  highlight: {
    type: Boolean,
    default: false
  },
  title: {
    type: String,
    default: null
  },
})
</script>

<style scoped>
.link-container {
  display: flex;
  flex-direction: column;
  gap: 5px;
  align-items: start;
  user-select: none;
}

.link-content {
  display: flex;
  gap: 5px;
  align-items: center;
}

.arrow {
  width: 55px;
  padding-bottom: 16px;
}

.navigation {
  font-weight: 600;
  padding: 3px;
  cursor: pointer;
  transition: font-size 0.2s ease;
}

.small {
  font-size: 14px;
}

.medium {
  font-size: 20px;
}

.large {
  font-size: 26px;
}

@media (hover: hover) {
  .navigation {
    background-image: linear-gradient(var(--gray), var(--gray));
    background-size: 0% 100%;
    background-repeat: no-repeat;
    background-position: left bottom;

    transition: background-size 0.35s cubic-bezier(0.25, 1, 0.5, 1),
      color 0.25s ease,
      font-size 0.2s ease;
  }

  .navigation:hover {
    background-size: 100% 100%;
    color: white;
  }
}


.active {
  background-color: var(--black);
  color: white;
}

.highlight {
  background-color: var(--blue);
  font-weight: 350;
  font-size: 1.4rem;
  line-height: 1;
  color: white;
}

.highlight-content {
  margin-top: 20px;
}
</style>