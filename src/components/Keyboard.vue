<template>
  <div class="main--keyboard">
      <div class="keyboard__frame">
          <div v-for="i in 4" class="keyboard__row" :key="i">
              <span v-for="y in 10" class="row__key" :key="y"></span>
          </div>
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
    width: 60%;
    height: 240px;
    margin: 10px auto 0 auto;
    display: flex;
    flex-wrap: wrap;
    border-right: 1px solid black;
    border-bottom: 1px solid black;
}
.keyboard__row {
    border-top: 1px solid black;
    width: 100%;
    height: 60px;
    display: flex;
    align-items: space-between;
}
.row__key {
    width: 10%;
    border-left: 1px solid black;
}
</style>
