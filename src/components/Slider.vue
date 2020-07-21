<template>
  <div class="main--slider">
    <div class="slider__slides">
      <div v-if="sliderNum === 1" class="slide slide__one">
          <div class="overlay">
              <h1>New York Based Software Developer</h1>
          </div>
        <video autoplay loop>
          <source src="/video.mp4" type="video/mp4" />
        </video>
      </div>
      <div v-if="sliderNum === 2" class="slide slide__two">
          <div class="overlay">
              <h2>Javascripter</h2>
          </div>
          <img src="sea.jpg" class="slide__img">
      </div>
      <div v-if="sliderNum === 3" class="slide slide__three">THREE</div>
    </div>
    <div class="slider__toggle">
      <div @click="sliderNum = 1">o</div>
      <div @click="sliderNum = 2">o</div>
      <div @click="sliderNum = 3">o</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider",
  components: {},
  data() {
    return {
      sliderNum: 1,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main--slider {
  height: 200px;
  width: 100%;
  position: relative;
  .slide {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    .slide__img {
        height: 100%;
        width: auto;
        transform: scale(1.5)
    }
    .overlay {
        //TODO make this snippet global extend
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,0.5);
        z-index: 1;
        h1,
        h2 {
            color: #fff;
        }
    }
    &__one {
      background: green;
      video {
          width: 100%;
          height: 100%;
          transform: scale(3)
      }
    }
    &__two {
      background: red;
    }
    &__three {
      background: blue;
    }
  }
  .slider__toggle {
    position: absolute;
    display: flex;
    width: 40px;
    height: 25px;
    bottom: 0;
    left: calc(50% - 20px);
    z-index: 2;
    color: #fff;
  }
}
</style>
