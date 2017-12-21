<template>
  <div>
    <quiz v-for="quiz in quizzes" :key="quiz.id" v-bind:quiz="quiz"></quiz>

    <div class="ui cards">
      <flash-card v-for="card in quizzes[0].cards" :key="card.id" v-bind:card="card"></flash-card>
    </div>
    
  </div>
</template>


<script>

import Quiz from './Quiz';
import FlashCard from './FlashCard';

export default {
  props: ['quizzes'],
  components: {
    Quiz,
    FlashCard,
  }
}
</script>


<style>

</style>
