<template>
  <div>
    <Header/>
    <Videos/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Videos from './components/Videos.vue'

export default {
  name: "App",
  components: {
    Header,
    Videos
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
