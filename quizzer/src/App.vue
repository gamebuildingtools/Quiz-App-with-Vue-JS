<template>
  <div id="app">
    <div class="ui centered card">
      <div class="content">
        <div class="header">
          {{title}}
        </div>
        <div class="meta">
          {{description}}
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
      title: "Chapter 1",
      description: "This is a sample description."
    }
  }
}
</script>

<style>
#app {
  margin-top: 60px;
}
</style>
