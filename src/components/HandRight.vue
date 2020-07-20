<template>
  <div class="right--hand">
      <div class="hand__base">
          
      </div>
  </div>
</template>

<script>
export default {
  name: "HandLeft",
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
    right: 0;
    width: 300px;
    height: 300px;
    background: tan;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
}
</style>
