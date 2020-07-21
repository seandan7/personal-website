<template>
  <div class="main--twobox">
    <div class="twobox__box">
      <h3>Lorem</h3>
      <p>
        Sit dolor amet. Lorem ipsum dolor sit, amet consectetur adipisicing
        elit.
      </p>
    </div>
    <div class="twobox__image">
      <img src="/sea.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Twobox",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main--twobox {
    margin-top: 16px;
}
.twobox__box {
  margin-top: 16px;
  color: #fff;
  padding: 5px;
}
img {
  width: 100%;
}

@media screen and (min-width: 600px) {
  .main--twobox {
    display: flex;
    justify-content: space-between;
    .twobox__box,
    .twobox__image {
      width: 47%;
    }
  }
}
</style>
