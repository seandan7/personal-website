<template>
  <div class="main--site">
    <div v-if="isOn">
      <div class="site__header">
        <div class="header__name">Sean Daniels</div>
        <div class="header__menu">
          <a href="#">About</a>
          <a href="#">Resume</a>
          <a href="#">Projects</a>
        </div>
      </div>
      <Slider />
      <Threebox />
    </div>
  </div>
</template>

<script>
import Slider from './Slider';
import Threebox from './Threebox';
export default {
  name: "Website",
  components: {
      Slider,
      Threebox
  },
  props: {
      isOn: Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.site__header {
  display: flex;
  justify-content: space-between;
  width: 100%;
  background: lightgray;
  padding: 5px 0;
  .header__name {
    color: black;
    font-size: 20px;
  }
  .header__menu {
    a {
      color: #000;
      text-decoration: none;
      padding: 0 5px;
    }
  }
}
</style>
