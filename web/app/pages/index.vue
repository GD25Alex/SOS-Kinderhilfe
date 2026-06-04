<template>
  <div>
    <Stage title="gemeinsam für <br/> neue perspektiven" image="image1" />
    <div class="container">
      <h1>SOS Wohnungslosenhilfe e.V.</h1>
      <p>Wohnungslose Menschen geraten in eine Krise, in der nichts mehr geht. Ohne Wohnung keine Adresse, ohne Adresse kein Arbeitsvertrag, kein Bankkonto, keine Chance auf einen neuen Mietvertrag. Und Geldbörse und Dokumente sind anfällig für Diebstahl und Verlust. Oft ist die einzige Hoffnung der Antrag auf Sozialleistungen. Doch man braucht bereits etwas Geld, um überhaupt Leistungen beantragen zu können. Das Sozialamt hilft den Menschen, auch mit Bereitstellung einer Unterkunft, kann jedoch nicht alle Kosten übernehmen. Der Verein „SOS Wohnungslosenhilfe e.V.“ wird daher ergänzend überbrückend in Notlagen tätig und unterstützt die Teilhabe wohnungsloser Menschen am gesellschaftlichen Leben.
      </p>

      <CImage :cols="1" fit="contain" :images="[{ 'title': 'Team', 'image': 'team' }]" />

      <h2 class="ac-callout">Gemeinsam wachsen</h2>
      <p>Um noch mehr Menschen helfen zu können, möchten wir unseren Verein weiter ausbauen.
Dafür sind wir auf Unterstützung angewiesen - jede Hilfe zählt. Ob durch Engagement oder Spenden: Wir freuen uns über jede Form der Unterstützung.
      </p>
    </div>
  </div>
</template>

<script setup>

const images = [
  { "title": "Image1", "image": "image6" },
  { "title": "Image2", "image": "image7" }
]
</script>

<style scoped>
.team {
  margin: 15px 0px;
  width: 100%;
  height: auto;
}
</style>