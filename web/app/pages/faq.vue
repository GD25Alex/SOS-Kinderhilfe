<template>
  <div>
    <Stage title="Jede Frage ist ein <br/> Schritt richtung Hilfe" image="image4" />
    <div class="container">
      <h1>FAQ</h1>
      <FaqItem :content="faq" />
    </div>

  </div>
</template>

<script setup>
const faq = [
  { question: "Wie arbeitet der Verein?", answer: "Die Vereinsmitglieder arbeiten ehrenamtlich, alle Spenden kommen wohnungslosen Menschen zugute." },
  { question: "Wer wird durch den Verein Unerstützt?", answer: "Der Verein arbeitet regional und unterstützt insbesondere wohnungslose Menschen vor Ort." },
  { question: "Wie wird meine Spende verwendet?", answer: " Ein großer Teil der Spenden wird für Lebensmittel und Kosten für die Wiederbeschaffung von Dokumenten sowie für Fahrkarten verwendet. Außerdem werden Projekte zur gesellschaftlichen Teilhabe wohnungsloser Menschen finanziert." },
  { question: "Kann ich meine Spende von der Steuer absetzen?", answer: "Ja, der Verein ist vom Finanzamt als gemeinnützig anerkannt, Spendenquittungen werden Ihnen gern ausgestellt. Bitte teilen Sie uns dazu das Datum Ihrer Spende und Ihre Kontaktdaten mit." },
]
</script>