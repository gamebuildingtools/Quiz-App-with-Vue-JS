<template>
  <div id="app">
    <quiz-list v-bind:quizzes="quizzes"></quiz-list>
    <create-quiz v-on:create-quiz="createQuiz"></create-quiz>
  </div>
</template>

<script>

import QuizList from './components/QuizList';
import CreateQuiz from './components/CreateQuiz';

export default {
  name: 'app',
  components: {
    QuizList,
    CreateQuiz
  },
  methods: {
    createQuiz(newQuiz) {
      const maxId = Math.max.apply(Math, this.quizzes.map(function(q) {return q.id}));
      const nextId = maxId + 1;
      this.quizzes.push({
        id: nextId,
        title: newQuiz.title,
        description: newQuiz.description,
        cards: []
      });
    }
  },
  data() {
    return {
      quizzes: [{
        id: 1,
        title: "Chapter 1",
        description: "This is a sample description.",
        cards: [
          {
            term: "Some Word",
            definition: "Some Definition"
          },
          {
            term: "Another Word",
            definition: "Another Definition of another word"
          }
        ]
      },{
        id: 2,
        title: "Chapter 2",
        description: "This is another sample description.",
        cards: [
          {

          }
        ]
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
