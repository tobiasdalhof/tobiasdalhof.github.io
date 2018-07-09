<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col">
          <resume />
        </div>
      </div>
    </div>
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

<style lang="scss">
@import 'bootstrap/scss/_functions.scss';
@import 'bootstrap/scss/_variables.scss';
@import 'bootstrap/scss/_mixins.scss';
@import 'bootstrap/scss/_utilities.scss';
@import 'bootstrap/scss/_grid.scss';
@import 'bootstrap/scss/_images.scss';

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
a {
  color: #03A9F4;
  &:hover {
    color: #B3E5FC;
  }
}
</style>
