<template>
  <div id="app">
    <resume />
  </div>
</template>

<script>
import resume from './components/Resume.vue'

export default {
  name: 'app',
  components: {
    resume
  }
}
</script>

<style>
body {
  padding: 0;
  margin: 0;
  font-family: 'Fira Mono', monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #FAFAFA;
  background-color: #212121;
  font-size: 16px;
}
</style>
