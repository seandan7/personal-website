<template>
  <div class="left--hand">
      <div class="hand__base">
          <div v-for="i in 4" :key="i">
              <Digit />
          </div>
      </div>
  </div>
</template>

<script>
import Digit from './Digit'
export default {
  name: "HandLeft",
  components: {
      Digit
  },
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hand__base {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 300px;
    height: 300px;
    background: tan;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
    display: flex;
    justify-content: space-between;
}
</style>
