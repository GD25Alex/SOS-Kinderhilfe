<template>
  <div>
    <Stage title="Um Unbürokratisch und <br/> unkompliziert helfen zu können" image="image2" />
    <div class="container">
      <h1>Verein</h1>
      <p class="callout">"Um unbürokratisch und unkompliziert helfen zu können"</p>
      <p>
Wohnungslose Menschen geraten in eine Krise, in der nichts mehr geht: Ohne Wohnung keine Adresse, ohne Adresse kein Arbeitsvertrag, kein Bankkonto, keine Chance auf einen neuen Mietvertrag. Und Geldbörse und Dokumente sind anfällig für Diebstahl und Verlust. Oft ist die einzige Hoffnung der Antrag auf Bürgergeld. Doch man braucht bereits etwas Geld, um überhaupt Leistungen beantragen zu können. Das Sozialamt hilft den Menschen, finanziert jedoch nicht alles.
      </p>

      <CImage :cols="1" fit="contain" :images="[{ 'title': 'Team', 'image': 'team' }]" />

      <p>Um unkompliziert und unbürokratisch helfen zu können, hat sich im Jahr <strong>2025</strong> der Verein <strong>„SOS Wohnungslosenhilfe e.V."</strong> gegründet.
<strong>Ziel des Vereins ist es, Spenden zu sammeln</strong> und wohnungslosen Menschen dabei zu helfen, nach Krisen wieder in ein selbstbestimmtes Leben zu starten, gesellschaftlichen Anschluss zu finden und sich wertvoll und gebraucht zu fühlen. Der Verein ist politisch und religiös unabhängig. Er verfolgt ausschließlich caritative Zwecke.
      </p>

      <h1>Mitglieder</h1>
      <h2 class="ac-callout">Das sind wir!</h2>
      <div class="people-container">
        <PersonCard v-for="person in people" :person="person" />
      </div>

      <h1>Unsere Satzung</h1>
      <Link highlight @click="openSatzung()">Hier zur Satzung</Link>
    </div>
  </div>
</template>

<script setup lang="ts">
import Link from '~/components/Link.vue';
import PersonCard from '~/components/PersonCard.vue';

const people = ref([
  { 'name': 'Birgit Grahl', 'role': 'Vorstandsvorsitzende', 'image': 'person1', 'text': 'Lorem illum ipsam eos at. Commodi, modi unde abveritatis harum a laborum tempora placeat voluptas consequuntur recusandae totam nulla tenetur expedita.Repudiandae atque aspernatur deserunt ducimus.' },
  { 'name': 'Marlene Neumann', 'role': 'Stellvertretende Vorstandsvorsitzende', 'image': 'person6', 'text': 'Lorem ipsum d unde abveritatis harum a laborum tempora placeat voluptas consequuntur recusandae totam nulla tenetur expedita.Repudiandae atque aspernatur deserunt ducimus.' },
  { 'name': 'Henriette R.', 'role': 'Praktikantin', 'image': 'person7', 'text': 'Lorem ipscusandae totam nulla tenetur expedita.Repudiandae atque aspernatur deserunt ducimus.' },
  { 'name': 'Ingo Schröder', 'role': 'Vorstandsmitglied', 'image': 'person2', 'text': 'Lorem iduntdolorem delectus a sint minima nemo dolorum, excepturi exercitationem illum ipsam eos at. Commodi, modi unde abveritatis harum a laborum tempora placeat voluptas consequuntur recusandae totam nulla tenetur expedita.Repudiandae atque aspernatur deserunt ducimus.' },
  { 'name': 'Thomas Leschke', 'role': 'Vereinsmitglied', 'image': 'person4', 'text': 'Lorem ipsum dolor sit amet consectetur, adipisicintur deserunt ducimus.' },
  { 'name': 'Sabine Wohlauf', 'role': 'Vereinsmitglied', 'image': 'person3', 'text': 'Lorem ipsum dolor sit amet cos consequuntur recusandae totam nulla tenetur expedita.Repudiandae atque aspernatur deserunt ducimus.' },
])

const openSatzung = () => {
  window.open('/downloads/satzung.pdf', '_blank', 'noopener,noreferrer')
}

</script>

<style scoped>
.team {
  margin: 15px 0px;
  width: 100%;
  height: auto;
}

.callout {
  font-size: 18px;
  font-weight: 700;
  padding-bottom: 20px;
}

.people-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 40px;
}
</style>