<template>
  <div>
    <quiz v-for="quiz in quizzes" :key="quiz.id" v-bind:quiz="quiz"></quiz>
  </div>
</template>


<script>

import Quiz from './Quiz';

export default {
  props: ['quizzes'],
  components: {
    Quiz
  }
}
</script>


<style>

</style>
