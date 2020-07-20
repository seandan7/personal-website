<template>
  <div class="digit--full">
      <div class="nail"></div>
      <div class="knuckle"></div>
  </div>
</template>

<script>
export default {
  name: "Digit",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.digit--full {
    height: 300px;
    width: 30px;
    background: tan;
    position: absolute;
    top: -100px;
}
</style>
