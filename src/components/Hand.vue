<template>
  <div :class="[whichHand + '--hand']">
      <div class="hand__base">
          <div v-for="i in 4" :key="i">
              <Digit :whichHand="whichHand" />
          </div>
      </div>
  </div>
</template>

<script>
import Digit from './Digit'
export default {
  name: "Hand",
  components: {
      Digit
  },
  props: {
    whichHand: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.hand__base {
    position: absolute;
    bottom: 0;
    width: 300px;
    height: 200px;
    background: tan;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
    display: flex;
    justify-content: space-between;
}
.right--hand {
  .hand__base {
    right: 0;
  }
}
.left--hand {
  .hand__base {
    left: 0;
  }
}
@media screen and (max-width: 600px) {
  .hand__base {
    display: none;
  }
}
</style>
