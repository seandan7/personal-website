<template>
  <div class="digit--full" :class="['digit--' + whichHand]">
    <div class="nail"></div>
    <div class="knuckle"></div>
  </div>
</template>

<script>
export default {
  name: "Digit",
  props: {
    whichHand: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.digit--full {
  height: 200px;
  width: 40px;
  background: tan;
  margin-top: -150px;
  border-top-left-radius: 25%;
  border-top-right-radius: 25%;
  position: relative;
  transition: transform 0.25s ease;
  .nail {
    width: 70%;
    height: 30px;
    margin: 0 auto;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
    border: 1px solid lightgray;
    background: burlywood;
  }
  .knuckle {
    position: absolute;
    height: 3px;
    width: 100%;
    top: 100px;
    border-top: 1px double #986643;
    border-bottom: 1px double #986643;
    padding: 3px 0;
  }
  &.digit--right {
    &:hover {
      transform: rotate(-3deg) scale(0.9);
    }
  }
  &.digit--left {
    &:hover {
      transform: rotate(3deg) scale(0.9);
    }
  }
}
</style>
