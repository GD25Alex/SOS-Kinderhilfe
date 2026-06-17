<template>
  <div>
    <Stage title="Hilfe, <br/> die Ankommt" image="image3" />
    <div class="container">
      <h1>Spendenmöglichkeiten</h1>
      <h2 class="ac-callout">Sie können immer helfen...</h2>

      <div class="icon-container">
        <IconCard v-for="option in options" :icon="option.icon" :title="option.title" />
      </div>

      <p>Unterstützen Sie als regionale Firma wohnungslose Menschen über Zuwendungen an den Verein im Rahmen von Sponsoring.
      </p>

      <h2 class="ac-callout">Sachspenden</h2>
      <p>Sie möchten Sachspenden spenden und direkt helfen? Kontaktieren Sie uns bei Fragen gerne per E-Mail oder Telefon.</p>

      <h2 class="ac-callout">Spendenkonto</h2>
      <div>
        <div v-for="(value, key) in spendenkonto" class="spenden-item">
          <p class="title">{{ key }}:</p>
          <p class="value">{{ value }}</p>
        </div>
      </div>
    </div>
  </div>
  < </template>

<script setup lang="ts">
import IconCard from '~/components/IconCard.vue';

const options = ref([
  { 'title': 'Sie können <strong> Geld </strong> für Lebensmittel, Hygieneartikel oder Projekte spenden', 'icon': 'money.svg' },
  { 'title': 'Stellen Sie gern auch <strong>Lebensmittel oder Hygieneartikel</strong> direkt zur Verfügung (auch kleine Mengen).', 'icon': 'hygiene.svg' },
  { 'title': 'In begrenztem Unfang wird <strong>gut erhaltene Kleidung für Männer</strong> (insbesondere Unterwäsche und Socken) gebraucht.', 'icon': 'socks.svg' },
  { 'title': 'Kontaktieren Sie uns gern, wenn Sie sich <strong>ehrenamtlich engangieren</strong> möchten.', 'icon': 'heart.svg' }
])


const spendenkonto = ref({
  "Inhaber": "SOS Wohnungslosenhilfe e.V.",
  "IBAN": "DE17 8505 0300 0221 3413 82",
  "BIC": "OSDDDE81XXX",
  "BANK": "Ostsächsische Sparkasse Dresden"
})

</script>

<style scoped>
.icon-container {
  display: flex;
  width: 100%;
  align-items: flex-start;
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

.spenden-item {
  display: flex;
  gap: 10px;
}

.title {
  text-transform: uppercase;
  font-weight: 700;
}

.value {
  font-weight: 700;
}

</style>