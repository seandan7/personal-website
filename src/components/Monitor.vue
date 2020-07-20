<template>
  <div class="main--monitor">
      <div class="monitor__frame">
          <div class="monitor"></div>
      </div>
  </div>
</template>

<script>
export default {
  name: "Monitor",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.monitor__frame {
    height: 600px;
    width: 80%;
    margin: 0 auto;
    background: lightblue;
    position: relative;
}
.monitor {
    background: #000;
    position: absolute;
    left: 20px;
    top: 20px;
    height: calc(100% - 40px);
    width: calc(100% - 40px)
}
</style>
