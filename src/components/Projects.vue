<template>
  <div class="main--projects">
    <div class="projects__project">
      <img src="/project-1.png" />
      <h3>Lorem Ipsum Dolor Sit</h3>
      <p><a href="#">View on Github</a></p>
    </div>
    <div class="projects__project">
        PROJECT SCREENSHOT
      <h3>Lorem Ipsum Dolor Sit</h3>
      <p><a href="#">View on Github</a></p>
    </div>
    <div class="projects__project">
        PROJECT SCREENSHOT
      <h3>Lorem Ipsum Dolor Sit</h3>
      <p><a href="#">View on Github</a></p>
    </div>
    <div class="projects__project">
        PROJECT SCREENSHOT
      <h3>Lorem Ipsum Dolor Sit</h3>
      <p><a href="#">View on Github</a></p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.projects__project {
  margin-top: 16px;
  img {
    width: 100%;
  }
}
@media screen and (min-width: 600px) {
    .main--projects {
        display: flex;
        flex-wrap: wrap;
    }
    .projects__project {
        width: 50%;
    }
}
</style>
