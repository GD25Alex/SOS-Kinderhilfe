<template>
  <div class="page-wrapper">
    <div class="site-layout">
      <Header />
      <main class="main-content">
        <NuxtPage />
      </main>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
.page-wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
  background-color: var(--bg-color);
  overflow-x: hidden;
}

.site-layout {
  display: flex;
  flex-direction: column;
  width: 100%;
  min-height: 100vh;
}

.main-content {
  flex-grow: 1;
  padding: 0;
}
</style>