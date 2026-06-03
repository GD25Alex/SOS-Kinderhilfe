<template>
  <div>
    <Stage title="gemeinsam für <br/> neue perspektiven" image="image1" />
    <h1>SOS Wohnungslosenhilfe e.V.</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt accusamus placeat deserunt molestias porro eius
      quidem unde, at neque delectus perspiciatis deleniti voluptatibus fuga praesentium? Quibusdam consequuntur rem,
      itaque nihil sint placeat iste ducimus laudantium dolorem voluptatum rerum ipsum reiciendis nesciunt omnis
      exercitationem! <strong>Aliquam mollitia itaque quas voluptates, </strong> laudantium ullam debitis eum tempore id
      amet cum
      blanditiis a at, quos rerum praesentium deleniti. Recusandae expedita nisi culpa voluptatibus. Illum, nesciunt
      pariatur dolore quaerat possimus cum inventore quam nesciunt. Dignissimos deserunt dolorem reprehenderit assumenda
      non, perspiciatis nisi. Inventore, maxime labore. Dolor tempora quo minima corrupti quisquam?
    </p>

    <CImage :cols="1" fit="contain" :images="[{ 'title': 'Team', 'image': 'team' }]" />

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt accusamus placeat deserunt molestias porro eius
      quidem unde, at neque delectus perspiciatis deleniti voluptatibus fuga praesentium? Quibusdam consequuntur rem,
      itaque nihil sint placeat iste ducimus laudantium dolorem voluptatum rerum ipsum reiciendis nesciunt omnis
      exercitationem! <strong>Aliquam mollitia itaque quas voluptates, </strong> laudantium ullam debitis eum tempore id
    </p>

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