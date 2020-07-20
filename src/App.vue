<template>
  <div id="app">
    <Monitor />
    <Keyboard />
  </div>
</template>

<script>
import Monitor from './components/Monitor.vue'
import Keyboard from './components/Keyboard.vue'

export default {
  name: 'App',
  components: {
    Monitor,
    Keyboard
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
