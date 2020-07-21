<template>
  <div class="main--site">
    <div v-if="isOn">
      <div class="site__header">
        <div class="header__name">Sean Daniels</div>
        <div class="header__menu">
          <a @click="page = 'main'" href="#">Home</a>
          <a @click="page = 'resume'" href="#">Resume</a>
          <a @click="page = 'projects'"  href="#">Projects</a>
        </div>
      </div>
      <div v-if="page === 'main'">
        <Slider />
        <Threebox />
        <Twobox />
      </div>
      <div v-if="page === 'resume'">
        <Resume />
      </div>
      <div v-if="page === 'projects'">
          <Projects />
      </div>
      <Footer />
    </div>
  </div>
</template>

<script>
import Slider from "./Slider";
import Threebox from "./Threebox";
import Twobox from "./Twobox";
import Footer from "./Footer";
import Resume from './Resume';
import Projects from './Projects';
export default {
  name: "Website",
  components: {
    Slider,
    Threebox,
    Twobox,
    Footer,
    Resume,
    Projects
  },
  data() {
      return {
          page: 'main'
      }
  },
  props: {
    isOn: Boolean,
  },
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
