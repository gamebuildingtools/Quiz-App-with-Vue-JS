<template>
  <div class="ui centered card">
    <div class="content">
      <div class="header">
        {{quiz.title}}
      </div>
      <div class="meta">
        {{quiz.description}}
      </div>
    </div>
    <div class="extra content">
      <span class="left floated">
        <i class="sticky note icon"></i>{{quiz.cards.length}}
      </span>
    </div>
  </div>
</template>


<script>
  export default {
    props: ['quiz'],
  }
</script>


<style>

</style>
