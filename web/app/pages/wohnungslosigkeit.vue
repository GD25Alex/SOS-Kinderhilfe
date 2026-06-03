<template>
  <div>
    <Stage title="Jeder braucht <br/> ein Zuhause" image="image1" />
    <h1>Wohnungslosigkeit</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt accusamus placeat deserunt molestias porro eius
      quidem unde, at neque delectus perspiciatis deleniti voluptatibus fuga praesentium? Quibusdam consequuntur rem,
      itaque nihil sint placeat iste ducimus laudantium dolorem voluptatum rerum ipsum reiciendis nesciunt omnis
      exercitationem! <strong>Aliquam mollitia itaque quas voluptates, </strong> laudantium ullam debitis eum tempore id
      amet cum
      blanditiis a at, quos rerum praesentium deleniti. Recusandae expedita nisi culpa voluptatibus. Illum, nesciunt
      pariatur dolore quaerat possimus cum inventore quam nesciunt. Dignissimos deserunt dolorem reprehenderit assumenda
      non, perspiciatis nisi. Inventore, maxime labore. Dolor tempora quo minima corrupti quisquam?
    </p>

    <CImage :images="images" />

    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt accusamus placeat deserunt molestias porro eius
      quidem unde, at neque delectus perspiciatis deleniti voluptatibus fuga praesentium? Quibusdam consequuntur rem,
      itaque nihil sint placeat iste ducimus laudantium dolorem voluptatum rerum ipsum reiciendis nesciunt omnis
      exercitationem! <strong>Aliquam mollitia itaque quas voluptates, </strong> laudantium ullam debitis eum tempore id
      amet cum
      blanditiis a at, quos rerum praesentium deleniti. Recusandae expedita nisi culpa voluptatibus. Illum, nesciunt
      pariatur dolore quaerat possimus cum inventore quam nesciunt. Dignissimos deserunt dolorem reprehenderit assumenda
      non, perspiciatis nisi. Inventore, maxime labore. Dolor tempora quo minima corrupti quisquam?
    </p>

    <Link title="Wir empfehlen ihnen diese Autoren und Bücher:" highlight>Hier gehts zu den Buchempfehlungen</Link>

    <CImage :cols="1" fit="contain" :images="[{ 'title': 'Test', 'image': 'image8' }]" />

  </div>
</template>

<script setup>
import Link from '~/components/Link.vue';

const images = [
  { "title": "Image1", "image": "image9" },
  { "title": "Image2", "image": "image10" }
]
</script>