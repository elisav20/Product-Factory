<template>
  <div class="intro">
    <div class="container">
      <Header />
      <div class="intro__inner">
        <div class="intro__content">
          <h1 class="intro__title">{{ title }}</h1>
          <div class="intro__subtitle">{{ subtitle }}</div>
          <p class="intro__text">{{ text }}</p>
          <a href="#" class="btn">Start Register</a>
        </div>
        <div class="intro__img">
          <img src="../assets/images/intro.png" alt="Intro" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./Header";

export default {
  components: {
    Header
  },
  data: () => ({
    title: "Product Design Course",
    subtitle: "Product Factory",
    text: `Learn how design thinking, user research, business vision and
            marketing, and finally designing and creating real digital products
            for real users.`
  })
};
</script>

<style lang="scss" scoped>
.intro {
  width: 100%;
  height: 75%;
  min-height: 780px;
  margin-bottom: 290px;
  background-color: #111;
  position: relative;

  &__inner {
    display: flex;
    justify-content: space-between;
    width: 100%;
    max-width: 1430px;
    height: 785px;
    margin: 0 auto;
    position: absolute;
    top: 170px;
    left: 0;
    right: 0;
    z-index: 10;
    background: #fff;
    border-radius: 25px;
    box-shadow: 0px 30px 45px 0px rgba(0, 0, 0, 0.13);
  }

  &__content {
    padding-top: 145px;
    padding-left: 130px;
  }

  &__title {
    font-size: 45px;
  }

  &__subtitle {
    width: 550px;
    height: 125px;
    padding-top: 15px;
    font-size: 35px;
    line-height: 45px;
    color: #8d8d8d;
    background-image: url("../assets/images/Product_Factory.png");
  }

  &__text {
    font-size: 23px;
    line-height: 50px;
  }

  .btn {
    display: block;
    width: 390px;
    padding: 15px 0;
    font-size: 24px;
    font-weight: bold;
    text-align: center;
    color: #fff;
    text-decoration: none;
    background-color: #f46632;
    border-radius: 15px;
    transition: all 0.2s linear;

    &:hover {
      background-color: rgb(54, 53, 53);
    }
  }

  &__img {
    padding: 110px 135px 110px 70px;
  }
}
</style>
