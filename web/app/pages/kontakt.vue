<template>
  <div>
    <Stage title="Hilfe, <br/> die ankommt" image="image5" />
    <h1>Kontakt</h1>
    <h2>So erreichen sie uns:</h2>

    <p><Strong>Adresse: </Strong>Florastraße 16, 01159 Dresden</p>
    <p><Strong>Telefon: </Strong>0351 27596371</p>
    <p><Strong>E-Mail: </Strong>sos.wohnungslosenhilfe.ev@gmail.com</p>

    <Link title="Sie möchten mehr über uns Erfahren:" highlight @click="navigateTo('/verein')">Mehr über den Verein
    </Link>
  </div>
</template>

<script setup lang="ts">
import Link from '~/components/Link.vue';
</script>