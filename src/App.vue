<template>
  <div id="app">
    <Monitor />
    <Keyboard />
    <HandLeft />
    <HandRight />
  </div>
</template>

<script>
import Monitor from './components/Monitor.vue'
import Keyboard from './components/Keyboard.vue'
import HandLeft from './components/HandLeft.vue'
import HandRight from './components/HandRight.vue'
export default {
  name: 'App',
  components: {
    Monitor,
    Keyboard,
    HandLeft,
    HandRight
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
  position: relative;
  height: 100vh;
}
</style>
