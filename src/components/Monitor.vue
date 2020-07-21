<template>
  <div class="main--monitor">
    <div class="monitor__frame">
      <div class="monitor">
        <Website :isOn="computerOn" />
      </div>
    </div>
    <div class="power-button" @click="computerToggle"></div>
  </div>
</template>

<script>
import Website from "./Website";
export default {
  name: "Monitor",
  components: {
    Website,
  },
  data() {
    return {
      computerOn: false,
    };
  },
  props: {
    msg: String,
  },
  methods: {
    computerToggle() {
      this.computerOn == true
        ? (this.computerOn = false)
        : (this.computerOn = true);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@keyframes glow {
  from {
    box-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #e60073,
      0 0 40px #e60073, 0 0 50px #e60073, 0 0 60px #e60073, 0 0 70px #e60073;
  }

  to {
    box-shadow: 0 0 20px #fff, 0 0 30px green, 0 0 40px green, 0 0 50px green,
      0 0 60px green, 0 0 70px green, 0 0 80px green;
  }
}
.main--monitor {
  position: relative;
}
.monitor__frame {
  height: 600px;
  width: 80%;
  max-width: 900px;
  margin: 0 auto;
  border: 20px solid lightblue;
  position: relative;
  overflow: scroll;
}
.monitor {
  background: #000;
  position: absolute;
  left: 20px;
  top: 20px;
  min-height: calc(100% - 40px);
  width: calc(100% - 40px);
}
.power-button {
  position: absolute;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 4px solid double;
  bottom: 0;
  left: calc(50% - 10px);
  animation: glow 1s ease-in-out infinite alternate;
  background: black;
}

/* width */
::-webkit-scrollbar {
  width: 6px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: limegreen;
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: darkgreen;
}
</style>
