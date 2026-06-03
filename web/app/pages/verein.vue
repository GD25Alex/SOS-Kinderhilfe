<template>
  <div>
    <Stage title="Um Unbürokratisch und <br/> unkompliziert helfen zu können" image="image2" />
    <h1>Verein</h1>
    <h2>"Um unbürokratisch und unkompliziert helfen zu können"</h2>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Adipisci magni voluptate nihil tenetur commodi ipsum
      voluptatum saepe tempora optio sunt, quam placeat neque? Delectus repudiandae doloremque maxime, velit corrupti
      iure nobis quos exercitationem non minima, recusandae laudantium soluta qui distinctio inventore quia? Quod vitae
      fugiat quos error ut non, corrupti beatae inventore at quia repellat odio unde? Quisquam vitae molestias
      doloremque libero in, dolor veritatis enim expedita eos. Nobis deserunt obcaecati, assumenda, laborum est,
      voluptates ex ullam eius facilis quae vel doloremque minus tempore accusamus animi aspernatur esse! Ab optio quos
      totam et inventore modi unde possimus? Inventore, unde nihil?
    </p>

    <CImage :cols="1" fit="contain" :images="[{ 'title': 'Team', 'image': 'team' }]" />

    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Animi veritatis distinctio possimus aut ex incidunt
      dolorem delectus a sint minima nemo dolorum, excepturi exercitationem illum ipsam eos at. Commodi, modi unde ab
      veritatis harum a laborum tempora placeat voluptas consequuntur recusandae totam nulla tenetur expedita.
      Repudiandae atque aspernatur deserunt ducimus.
    </p>

    <h1>Mitglieder</h1>
    <h2>Das sind wir!</h2>
    <div class="people-container">
      <PersonCard v-for="person in people" :person="person" />
    </div>

    <h1>Unsere Satzung</h1>
    <Link highlight @click="openSatzung()">Hier zur Satzung</Link>


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

.people-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
  gap: 20px;
}
</style>