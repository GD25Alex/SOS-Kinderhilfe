<template>
  <div class="faq-wrapper">
    <div v-for="(item, index) in content" :key="index">
      <div class="item-container">

        <div class="question-container" @click="toggleItem(index)">
          <div class="question">
            <h2>{{ index + 1 }}.</h2>
            <h2>{{ item.question }}</h2>
          </div>
          <p class="action">{{ activeIndex === index ? '−' : '+' }}</p>
        </div>

        <div class="answer-wrapper" :class="{ 'open': activeIndex === index }">
          <div class="answer-container">
            <p>{{ item.answer }}</p>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  content: {
    type: Array,
    default: () => [
      { question: "Was bedeutet Wohnungslosigkeit?", answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum consequuntur officia, sequi perferendis repudiandae odio eos fugit cum animi corrupti corporis autem maxime aliquid beatae eius possimus impedit id necessitatibus sapiente explicabo voluptates cumque dolorem dolore. Delectus eius culpa accusantium voluptatum pariatur dicta voluptatem recusandae est! Inventore amet unde expedita eaque commodi culpa deserunt quidem soluta mollitia magnam voluptas iusto aperiam, blanditiis quasi odio atque adipisci. Nisi fugiat nam vero nostrum, ab inventore, magni provident aspernatur quae obcaecati praesentium itaque odio totam officiis quo asperiores. Adipisci labore dolorum nemo vero voluptatibus omnis nam maiores unde amet obcaecati quisquam facilis, cum fuga voluptatum cupiditate vitae a sequi similique iusto illum perspiciatis explicabo repellendus. Corrupti natus eaque sequi tenetur, labore esse repellat est optio maxime error quidem ipsam saepe perferendis voluptatem corporis. Quo unde delectus hic architecto magni ab quasi ex doloremque, a impedit dignissimos provident mollitia rerum aperiam porro? Commodi error, ut animi dolorem nostrum molestias soluta quos repellat harum voluptate eveniet iste distinctio velit cupiditate magni obcaecati ullam ex a vel laudantium praesentium hic ipsa. Cumque magni sunt cupiditate nobis illum odio repudiandae ipsam incidunt quisquam, facilis asperiores et voluptatibus nihil minus quae voluptates optio accusamus, doloribus quia id. Ipsam." },
      { question: "Zweite Frage?", answer: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum consequuntur officia, sequi perferendis repudiandae odio eos fugit cum animi corrupti corporis autem maxime aliquid beatae eius possimus impedit id necessitatibus sapiente explicabo voluptates cumque dolorem dolore. Delectus eius culpa accusantium voluptatum pariatur dicta voluptatem recusandae est! Inventore amet unde expedita eaque commodi culpa deserunt quidem soluta mollitia magnam voluptas iusto aperiam, blanditiis quasi odio atque adipisci. Nisi fugiat nam vero nostrum, ab inventore, magni provident aspernatur quae obcaecati praesentium itaque odio totam officiis quo asperiores. Adipisci labore dolorum nemo vero voluptatibus omnis nam maiores unde amet obcaecati quisquam facilis, cum fuga voluptatum cupiditate vitae a sequi similique iusto illum perspiciatis explicabo repellendus. Corrupti natus eaque sequi tenetur, labore esse repellat est optio maxime error quidem ipsam saepe perferendis voluptatem corporis. Quo unde delectus hic architecto magni ab quasi ex doloremque, a impedit dignissimos provident mollitia rerum aperiam porro? Commodi error, ut animi dolorem nostrum molestias soluta quos repellat harum voluptate eveniet iste distinctio velit cupiditate magni obcaecati ullam ex a vel laudantium praesentium hic ipsa. Cumque magni sunt cupiditate nobis illum odio repudiandae ipsam incidunt quisquam, facilis asperiores et voluptatibus nihil minus quae voluptates optio accusamus, doloribus quia id. Ipsam." }
    ]
  }
})

const activeIndex = ref(null)

const toggleItem = (index) => {
  if (activeIndex.value === index) {
    activeIndex.value = null
  } else {
    activeIndex.value = index
  }
}
</script>

<style scoped>
.faq-wrapper {
  margin-bottom: 20px;
}

.item-container {
  display: flex;
  flex-direction: column;
  padding-bottom: 10px;
  border-bottom: 3px solid var(--blue);
}

.question-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
}

.question {
  display: flex;
  gap: 5px;
}

.action {
  font-size: 40px;
  user-select: none;
}

.answer-wrapper {
  display: grid;
  grid-template-rows: 0fr;
  transition: grid-template-rows 0.3s ease-out;
  overflow: hidden;
}

.answer-wrapper.open {
  grid-template-rows: 1fr;
}

.answer-container {
  min-height: 0;
}

.answer-container p {
  margin: 10px;
  border: 2px solid var(--blue);
  padding: 5px;
}
</style>