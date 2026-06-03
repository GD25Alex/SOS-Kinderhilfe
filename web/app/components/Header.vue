<template>
  <div class="header-wrapper">
    <div class="image-container">
      <img src="/images/logo.png" alt="Unser Logo" class="logo" @click="navigateTo('/')" />
      <img v-if="!isDesktop" :src="`/images/symbols/${showMenu ? 'close' : 'menu'}.png`" class="menu"
        @click="showMenu = !showMenu" />
    </div>
    <div class="items" v-if="isDesktop">
      <Link v-for="link in links" :key="link.url" :active="route.name === link.url || route.path === '/' + link.url"
        @click="navigateTo(link.url)">
        {{ link.title }}
      </Link>
    </div>
    <Transition name="slide">
      <div v-if="!isDesktop && showMenu" class="mobile-wrapper">
        <div class="link-container">
          <Link v-for="link in links" :key="link.url" :active="route.name === link.url || route.path === '/' + link.url"
            @click="navigateTo(link.url); showMenu = false">
            {{ link.title }}
          </Link>
        </div>

      </div>
    </Transition>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
import Link from './Link.vue'
import { ref, onMounted, onUnmounted } from 'vue'

const route = useRoute()

const links = ref([
  { 'title': "Home", 'url': '' },
  { 'title': "Wohnungslosigkeit", 'url': 'wohnungslosigkeit' },
  { 'title': "Verein", 'url': 'verein' },
  { 'title': "Spenden", 'url': 'spenden' },
  { 'title': "FAQ", 'url': 'faq' },
  { 'title': "Kontakt", 'url': 'kontakt' },
])

const isDesktop = ref(true)
const showMenu = ref(false)

const checkScreenSize = () => {
  isDesktop.value = window.innerWidth >= 1024
  if (isDesktop.value) showMenu.value = false
}

watch(showMenu, (isOpen) => {
  if (isOpen) {
    document.documentElement.style.overflow = 'hidden'
    document.body.style.overflow = 'hidden'
  } else {
    document.documentElement.style.overflow = ''
    document.body.style.overflow = ''
  }
})

onMounted(() => {
  checkScreenSize()
  window.addEventListener('resize', checkScreenSize)
})

onUnmounted(() => {
  window.removeEventListener('resize', checkScreenSize)
})
</script>

<style scoped>
.header-wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 10px 0px;
  align-items: center;
  background-color: var(--bg-color);
  justify-content: space-between;
}

.mobile-wrapper {
  position: fixed;
  top: 80px;
  left: 0;
  height: calc(100vh - 80px);
  width: 100vw;
  background-color: var(--white);
  z-index: 999;
  overflow: hidden;
}

.link-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.items {
  display: flex;
  justify-content: space-between;
  width: 80%;
  align-items: center;
}

.image-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  width: 280px;
  height: auto;
  max-width: 100%;
  cursor: pointer;
}

.menu {
  width: 20px;
  height: auto;
  max-width: 25px;
  cursor: pointer;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.35s ease-in-out, opacity 0.25s ease;
}

.slide-enter-from,
.slide-leave-to {
  transform: translateY(-20px);
  opacity: 0;
}
</style>