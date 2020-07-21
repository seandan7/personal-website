<template>
  <div class="main--threebox">
    <div class="threebox__box">
        <h3>Lorem</h3>
        <p>Sit dolor amet. Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
    </div>
    <div class="threebox__box">
        <h3>Ipsum</h3>
        <p>Sit dolor amet. Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
    </div>
    <div class="threebox__box">
        <h3>Dolor</h3>
        <p>Sit dolor amet. Lorem ipsum dolor sit, amet consectetur adipisicing elit.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Threebox",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main--threebox {
    padding: 20px 0;
}
    .threebox__box {
        margin-top: 16px;
        background: yellow;
        color: #000;
        padding: 5px;
    }

    @media screen and (min-width: 600px) {
        .main--threebox {
            display: flex;
            justify-content: space-between;
            .threebox__box {
                width: 30%;
            }
        }
    }
</style>
