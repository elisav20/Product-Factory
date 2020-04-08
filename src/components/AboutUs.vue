<template>
  <div class="container">
    <div class="about-us">
      <div class="about-us__inner">
        <div class="about-us__header">
          <div class="about-us__title">{{ title }}</div>
          <span class="about-us__social">
            <img
              class="about-us__social-icon"
              src="../assets/images/facebook-square-brands.png"
              alt="facebook"
            />
            <img
              class="about-us__social-icon"
              src="../assets/images/twitter-brands.png"
              alt="twitter"
            />
            <img
              class="about-us__social-icon"
              src="../assets/images/instagram-brands(1).png"
              alt="instagram"
            />
          </span>
        </div>
        <p class="about-us__text">{{ text }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "AboutUs",
  data: () => ({
    title: "About Us",
    text: `Today, given the economic and labor market conditions, the best and least risky way to invest is
          to invest in personal assets and skills. UI / UX Product Design Course covers all aspects of product
          design from product thinking and design to user-centric research and product research and business
          vision and digital marketing to product designers and creators, designing the end-user experience and
           interface of the product and how to deliver it. Includes.`
  })
};
</script>

<style lang="scss" scoped>
.about-us {
  width: 100%;
  position: relative;
  margin-top: 450px;

  &__inner {
    width: 100%;
    max-width: 1430px;
    margin: 0 auto;
    padding: 40px 120px 75px;
    position: relative;
    background: #fff;
    border-radius: 25px;
    box-shadow: 0px 30px 45px 0px rgba(0, 0, 0, 0.13);

    &::before {
      display: block;
      content: url("../assets/images/about_us.png");
      position: absolute;
      top: -150px;
      left: 120px;
      z-index: 10;
    }
  }

  &__header {
    display: flex;
    justify-content: flex-end;
  }

  &__title {
    display: inline-block;
    padding-top: 75px;
    width: 350px;
    height: 160px;
    font-size: 32px;
    line-height: 43px;
    font-weight: bold;
    text-align: center;
    background-image: url("../assets/images/About.png");
    background-size: cover;
    background-repeat: no-repeat;
  }

  &__social {
    display: flex;
    flex-direction: column;
    margin-left: 80px;
    padding-top: 10px;

    &-icon {
      margin-bottom: 30px;
    }
  }

  &__text {
    display: block;
    margin-top: 50px;
    padding-right: 42px;
    font-size: 19px;
    line-height: 50px;
  }
}
</style>
