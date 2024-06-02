<template>
  <div id="app">
    <CvComponent />
  </div>
</template>

<script>
import CvComponent from './components/CvComponent.vue';

export default {
  name: 'App',
  components: {
    CvComponent,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
