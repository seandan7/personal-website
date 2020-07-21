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
    </div>
  </div>
</template>

<script>
export default {
  name: "Website",
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
  .header__name {
    color: lawngreen;
    font-size: 20px;
  }
  .header__menu {
    a {
      color: #fff;
      text-decoration: none;
      padding: 0 5px;
    }
  }
}
</style>
