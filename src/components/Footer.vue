<template>
  <div class="main--footer">
      <div class="footer__form">
      </div>
      <div class="footer__contact">
          <h4>Contact Me</h4>
          <p>Email: sean@seandaniels.com</p>
          <p>LinkedIn: <a href="https://www.linkedin.com/in/sean-daniels-nyc">linkedin.com/in/sean-daniels-nyc</a></p>
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
.main--footer {
    margin-top: 16px;
    color: #fff;
    a {
        color: #fff;
    }
}

@media screen and (min-width: 600px) {
  .main--footer {
    display: flex;
    justify-content: space-between;
    .footer__form,
    .footer__contact {
      width: 50%;

    }
  }
}
</style>
