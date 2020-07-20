<template>
  <div class="main--keyboard">
      <div class="keyboard__frame">
      </div>
  </div>
</template>

<script>
export default {
  name: "Keyboard",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.keyboard__frame {
    background: lightgray;
    width: 100%;
    height: 250px;
}
</style>
