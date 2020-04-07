<template>
  <div class="header">
    <div class="header__inner">
      <a href="#">
        <img src="../assets/images/Logo.png" alt="Logo" />
      </a>
      <nav class="nav">
        <template v-for="page in pages">
          <a :href="page" class="nav__link" :key="page">{{ page }}</a>
        </template>
        <a href="#" class="btn">Register</a>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data: () => ({
    pages: [
      "Projects",
      "Partners",
      "Faq",
      "Masters",
      "Classes",
      "Course Experience",
      "About Us"
    ]
  })
};
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 50px;
  z-index: 1000;
  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 50px;
  }
}
.nav {
  display: flex;
  align-items: center;
  font-size: 14px;
  line-height: 26px;

  &__link {
    margin-right: 75px;
    color: #fff;
    text-decoration: none;
    transition: all 0.1s linear;

    &:hover {
      border-bottom: 1px solid #fff;
    }
  }
}

.btn {
  padding: 10px 45px;
  text-align: center;
  color: #fff;
  text-decoration: none;
  background-color: rgba($color: #fff, $alpha: 0.16);
  border-radius: 30px;
  transition: all 0.2s linear;

  &:hover {
    background: #fff;
    color: #333;
  }
}
</style>
