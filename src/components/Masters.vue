<template>
  <div class="container">
    <div class="master">
      <div class="master__title">{{ title }}</div>
      <div class="master__inner">
        <div class="master__item" v-for="(value, key) in masters" :key="key">
          <div class="master__info">
            <img class="master__img" :src="getPic(value.id)" :alt="value.name" />
            <div class="master__content">
              <div class="master__social">
                <a class="master__social-link" href="#">
                  <img src="../assets/images/twitter.png" alt="twitter">
                </a>
                <a class="master__social-link" href="#">
                  <img src="../assets/images/facebook.png" alt="facebook">
                </a>
                <a class="master__social-link" href="#">
                  <img src="../assets/images/instagram-brands.png" alt="instagram">
                </a>
              </div>
            </div>
          </div>
          <h3 class="master__name">{{ value.name }}</h3>
          <p class="master__position">{{ value.position }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Masters",
  data: () => ({
    title: "Masters",
    masters: {
      1: {
        id: 1,
        name: "Shervin Mashayekh",
        position: "Additive Product Manager",
      },
      2: {
        id: 2,
        name: "Kianoosh Keyghobadi",
        position: "Product Manager at Digikala",
      },
      3: {
        id: 3,
        name: "Hossein Vahdani",
        position: "Content marketing specialist",
      },
      4: {
        id: 4,
        name: "Ali Babaei",
        position: "Product design consultant",
      },
      5: {
        id: 5,
        name: "Kiarash Amalivand",
        position: "Head of product at Ap",
      },
      6: {
        id: 6,
        name: "Hesam Keramati",
        position: "Product designer at Bazaar",
      },
      7: {
        id: 7,
        name: "Hassan Hemati",
        position: "Product designer at Alibaba",
      },
      8: {
        id: 8,
        name: "Sheragim Moradi",
        position: "Marketing manager",
      },
      9: {
        id: 2,
        name: "Hadi Ebnodin",
        position: "Service designer",
      },
      10: {
        id: 10,
        name: "Moslem Ebrahimi",
        position: "Typeface designer",
      },
    },
  }),
  methods: {
    getPic(id) {
      return require(`../assets/images/masters/${id}.jpg`);
    },
  },
};
</script>

<style lang="scss" scoped>
.master {
  background: #fff;
  border-radius: 25px;
  box-shadow: 0px 30px 45px 0px rgba(0, 0, 0, 0.13);
  &__title {
    width: 445px;
    height: 160px;
    margin: 0 auto 70px;
    padding-top: 80px;
    font-size: 32px;
    font-weight: bold;
    line-height: 43px;
    text-align: center;
    background-image: url("../assets/images/Masters.png");
    background-size: cover;
  }

  &__inner {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  &__item {
    width: 20%;
    margin-bottom: 70px;
    text-align: center;

    &:hover .master__content {
      opacity: 1;
    }
  }

  &__info {
    position: relative;
  }

  &__content {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 200px;
    height: 200px;
    background: rgba(0, 0, 0, 0.5);
    border-radius: 10px;
    position: absolute;
    top: 0;
    left: 43px;
    z-index: 5;
    opacity: 0;
    transition: all .2s linear;
  }

  &__social {
    display: flex;
    align-items: center;

    &-link {
      padding: 0 15px;
    }
  }

  &__img {
    position: relative;
  }

  &__name {
    font-size: 18px;
    font-weight: bold;
    line-height: 32px;
  }

  &__position {
    font-size: 16px;
    line-height: 20px;
  }
}
</style>
