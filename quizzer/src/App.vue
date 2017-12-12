<template>
  <div id="app">
    <div v-for="quiz in quizzes" class="ui centered card">
      <div class="content">
        <div class="header">
          {{quiz.title}}
        </div>
        <div class="meta">
          {{quiz.description}}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {},
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
