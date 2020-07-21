<template>
  <div :class="[whichHand + '--hand']">
    <div class="hand__base" :class="{
      'active-left': isActiveLeft,
      'active-right': isActiveRight
    }">
      <div v-for="i in 4" :key="i">
        <Digit :whichHand="whichHand" />
      </div>
    </div>
  </div>
</template>

<script>
import Digit from "./Digit";
export default {
  name: "Hand",
  components: {
    Digit,
  },
  data() {
    return {
      isActiveLeft: false,
      isActiveRight: false,
      keysThatMatterLeft: ["q", "a", "z"],
      keysThatMatterRight:["p", "l", "m"]
    };
  },
  props: {
    whichHand: String,
  },
  mounted() {
    document.addEventListener("keydown", this.toggleActive);
  },
  methods: {
    toggleActive(e) {
      if (this.keysThatMatterLeft.includes(e.key)) {
        this.isActiveLeft ? (this.isActiveLeft = false) : (this.isActiveLeft = true);
      }
      if (this.keysThatMatterRight.includes(e.key)) {
        this.isActiveRight ? (this.isActiveRight = false) : (this.isActiveRight = true);
      }
    }
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
    transition: right .25s ease;
    &.active-right {
      right: 300px;
    }
  }
}
.left--hand {
  .hand__base {
    left: 0;
    transition: left .25s ease;
    &.active-left {
      left: 300px;
    }
  }
}
@media screen and (max-width: 600px) {
  .hand__base {
    display: none;
  }
}
</style>
