<template>
  <div id="app">
    <Monitor />
    <Keyboard />
    <Hand :whichHand="'left'" />
    <Hand :whichHand="'right'" />
  </div>
</template>

<script>
import Monitor from './components/Monitor.vue'
import Keyboard from './components/Keyboard.vue'
import Hand from './components/Hand.vue'
export default {
  name: 'App',
  components: {
    Monitor,
    Keyboard,
    Hand
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Red Rose', cursive;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: relative;
  min-height: 100vh;
  background: #2c3e50;
}
</style>
