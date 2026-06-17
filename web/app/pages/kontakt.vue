<template>
  <div>
    <Stage title="Hilfe, <br/> die ankommt" image="image5" />
    <div class="container">
      <h1>Kontakt</h1>
      <h2 class="ac-callout">So erreichen sie uns:</h2>

      <p><Strong>Adresse: </Strong>Florastraße 16, 01159 Dresden</p>
      <p><Strong>Telefon: </Strong>0351 27596371</p>
      <p><Strong>E-Mail: </Strong>sos.wohnungslosenhilfe.ev@gmail.com</p>

      <h2 style="margin-top: 20px;" class="ac-callout">Sie möchten mehr über uns Erfahren:</h2>
      <Link highlight @click="navigateTo('/verein')">Mehr über den Verein</Link>
    </div>

  </div>
</template>

<script setup lang="ts">
import Link from '~/components/Link.vue';
</script>