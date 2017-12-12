<template>
  <div>
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
  props: ['quizzes']
}
</script>


<style>

</style>
