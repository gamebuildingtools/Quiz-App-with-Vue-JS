<template>
  <div id="app">
    <quiz-list v-bind:quizzes="quizzes"></quiz-list>
  </div>
</template>

<script>

import QuizList from './components/QuizList';

export default {
  name: 'app',
  components: {
    QuizList
  },
  data() {
    return {
      quizzes: [{
        title: "Chapter 1",
        description: "This is a sample description."
      },{
        title: "Chapter 2",
        description: "This is another sample description."
      }]
    }
  }
}
</script>

<style>
#app {
  margin-top: 60px;
}
</style>
