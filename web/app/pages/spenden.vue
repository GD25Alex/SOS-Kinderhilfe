<template>
  <div>
    <Stage title="Hilfe, <br/> die Ankommt" image="image3" />
    <h1>Spendenmöglichkeiten</h1>
    <h2>Sie können immer helfen...</h2>

    <div class="icon-container">
      <IconCard v-for="option in options" :icon="option.icon" :title="option.title" />
    </div>

    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Deleniti quasi quibusdam asperiores animi id
      repudiandae distinctio dolorum quidem aliquid. Quibusdam.
    </p>

    <h3>Sachspenden</h3>
    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Praesentium, voluptatem.</p>

    <h3>Spendenkonto</h3>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Animi labore a aspernatur nobis quis cumque facilis
      pariatur, aperiam qui soluta.</p>
  </div>
</template>

<script setup lang="ts">
import IconCard from '~/components/IconCard.vue';

const options = ref([
  { 'title': 'Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden', 'icon': 'handshake' },
  { 'title': 'Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden', 'icon': 'handshake' },
  { 'title': 'Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden', 'icon': 'handshake' },
  { 'title': 'Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden', 'icon': 'handshake' }
])

</script>

<style scoped>
.icon-container {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 25px;
  padding-bottom: 12px;
  overflow-x: auto;
  scroll-behavior: smooth;
  -webkit-overflow-scrolling: touch;
}

.icon-container::-webkit-scrollbar {
  height: 6px;
}

.icon-container::-webkit-scrollbar-thumb {
  background-color: var(--lightblue);
  border-radius: 10px;
}
</style>