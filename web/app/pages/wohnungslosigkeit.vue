<template>
  <div>
    <Stage title="Jeder braucht <br/> ein Zuhause" image="image6" />
    <div class="container">
      <h1>Wohnungslosigkeit</h1>
      <p> Ist es für Sie vorstellbar, ein. zwei. drei oder sogar <strong>zehn Jahre ohne Wohnung</strong> zu leben? Zunächst finden Sie vielleicht noch Unterschlupf bei Freunden oder Verwandten, doch im Laufe der Zeit wird Ihnen bewusst, dass Sie Ihre Mitmenschen stören. Und Sie machen sich auf den Weg...

Menschen, die - häufig nach langer Odyssee - in einem Heim landen, haben um ihr Überleben gekämpft, sind erschöpft, aufgerieben und <strong>haben oft unglaubliche Geschichten erlebt</strong>. Wie Franzi, die in Papiercontainern schlief, um nicht zu erfrieren; Lothar, der verwitwete Lehrer, dessen Lager im Park war oder Oskar und andere <strong>Jugendliche</strong>, die nach Heimerziehung auf der Straße stehen und nicht wissen, wie und wo es weitergehen soll..
      </p>

      <CImage :images="images" />

      <p>Wohnungslosigkeit bringt gravierende Entbehrungen mit sich, und auf lange Sicht macht sie <strong>krank</strong>. Die Betroffenen weisen im Vergleich zur Durchschnittsbevölkerung 
        ein Vielfaches an körperlichen oder seelischen Erkrankungen auf. Sie leben in ständiger Gefahr, Gewalt zu erfahren und werden von der gesellschaftlichen Mitte gemieden. 
        Alkohol oder Drogen sind keine empfehlenswerten Unterstützer, aber sie können das Leben erträglicher machen. Wohnungslosigkeit hat gravierende Auswirkungen auf das Leben eines Menschen. <strong>Und es ist nicht so leicht, wieder in die Gesellschaft zurückzukommen, wie man vielleicht denkt</strong>.
        Einige ehemals wohnungslose Menschen haben Bücher über ihre Erfahrungen auf der Straße und die schwere Rückkehr in die Gesellschaft geschrieben.
      </p>

      <Link title="Wir empfehlen ihnen diese Autoren und Bücher:" highlight>Hier gehts zu den Buchempfehlungen</Link>

      <CImage :cols="1" fit="contain" :images="[{ 'title': 'Test', 'image': 'image8' }]" />
    </div>
  </div>
</template>

<script setup>
import Link from '~/components/Link.vue';

const images = [
  { "title": "Image1", "image": "image9" },
  { "title": "Image2", "image": "image10" }
]
</script>