<template>
  <div class="main--keyboard">
    <div class="keyboard__frame">
      <div v-for="i in 3" class="keyboard__row" :key="i">
        <span v-for="y in 10" class="row__key" :key="y">
          <span v-if="i == 1 && y == 1">q</span>
          <span v-if="i == 1 && y == 10">p</span>
          <span v-if="i == 2 && y == 1">a</span>
          <span v-if="i == 2 && y == 10">l</span>
          <span v-if="i == 3 && y == 1">z</span>
          <span v-if="i == 3 && y == 10">m</span>
        </span>
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
<style scoped lang="scss">
@-webkit-keyframes glow {
  from {
    text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #e60073,
      0 0 40px #e60073, 0 0 50px #e60073, 0 0 60px #e60073, 0 0 70px #e60073;
  }

  to {
    text-shadow: 0 0 20px #fff, 0 0 30px green, 0 0 40px green,
      0 0 50px green, 0 0 60px green, 0 0 70px green, 0 0 80px green;
  }
}
.keyboard__frame {
  background: lightgray;
  width: 60%;
  height: 180px;
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
  &:hover {
    background: lightblue;
  }
  span {
    animation: glow 1s ease-in-out infinite alternate;
  }
}

@media screen and (max-width: 600px) {
  .keyboard__frame {
    height: 150px;
    .keyboard__row {
      height: 25px;
    }
  }
}
</style>
