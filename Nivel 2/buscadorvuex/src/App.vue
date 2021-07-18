<template>
  <div id="app">
    <div class="container">
      <moviesApp></moviesApp>
    </div>
  </div>
</template>

<script>
import moviesApp from './components/moviesApp';

export default {
  name: 'App',
  components: {
    moviesApp
  }
}
</script>

<style lang="scss">
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
