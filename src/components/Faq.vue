<template>
  <div class="container">
    <div class="faq">
      <div class="faq__title">
        <div class="faq__text">{{ title }}</div>
      </div>

      <div class="accordion" id="accordion">
        <div
          class="accordion-item"
          v-for="(value, key) in questions"
          :key="key"
        >
          <p class="accordion-item-head" v-on:click="accordion">
            {{ value.question }}
          </p>

          <div class="accordion-item-body">{{ value.response }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Faq",
  data: () => ({
    title: "Frequently Asked Questions",
    questions: {
      1: {
        id: 1,
        question: "Does this course need any special requirements?",
        response: `Integer tincidunt. Maecenas ullamcorper, dui et placerat feugiat, eros pede varius nisi, condimentum
                   viverra felis nunc et lorem. Duis leo. Suspendisse eu ligula. Fusce commodo aliquam arcu.`
      },
      2: {
        id: 2,
        question:
          "Who are the audiences of the product design period of the product factory?",
        response: `Integer tincidunt. Maecenas ullamcorper, dui et placerat feugiat, eros pede varius nisi, condimentum
                   viverra felis nunc et lorem. Duis leo. Suspendisse eu ligula. Fusce commodo aliquam arcu.`
      },
      3: {
        id: 3,
        question: "Is it possible to pay by installments?",
        response: `Integer tincidunt. Maecenas ullamcorper, dui et placerat feugiat, eros pede varius nisi, condimentum
                   viverra felis nunc et lorem. Duis leo. Suspendisse eu ligula. Fusce commodo aliquam arcu.`
      },
      4: {
        id: 4,
        question: "Can I start an internship after I finish the course?",
        response: `Integer tincidunt. Maecenas ullamcorper, dui et placerat feugiat, eros pede varius nisi, condimentum
                   viverra felis nunc et lorem. Duis leo. Suspendisse eu ligula. Fusce commodo aliquam arcu.`
      },
      5: {
        id: 5,
        question: "What should I do after I finish the course?",
        response: `Integer tincidunt. Maecenas ullamcorper, dui et placerat feugiat, eros pede varius nisi, condimentum
                   viverra felis nunc et lorem. Duis leo. Suspendisse eu ligula. Fusce commodo aliquam arcu.`
      }
    }
  }),
  methods: {
    accordion: function(event) {
      event.target.classList.toggle("active");
    }
  }
};
</script>

<style lang="scss" scoped>
.faq {
  position: relative;

  &__title {
    width: 400px;
    height: 250px;
    margin: 0 auto 100px;
    padding-top: 120px;
    font-size: 32px;
    font-weight: bold;
    line-height: 43px;
    background-image: url(../assets/images/FAQ.png);
    background-size: cover;
  }

  &__text {
    width: 500px;
    position: absolute;
    top: 125px;
    left: 54%;
    z-index: 2;
    transform: translateX(-54%);
  }
}

.accordion-item {
  position: relative;
  margin-bottom: 30px;
}

.accordion-item-head {
  margin-bottom: 5px;
  padding: 25px 60px;
  font-size: 21px;
  font-weight: normal;
  line-height: 33px;
  background: #fff;
  border-radius: 25px;
  box-shadow: 0px 10px 45px 0px rgba(0, 0, 0, 0.13);
  cursor: pointer;
}

.accordion-item-head:after {
  content: url("../assets/images/plus.png");
  display: block;
  width: 35px;
  height: 35px;
  position: absolute;
  right: 45px;
  top: 51%;
  transform: translateY(-51%);
}

.accordion-item-head.active:after {
  content: " | ";
  position: absolute;
  top: 13%;
  right: 45px;
  transform: translateY(-13%);
  transform: rotate(90deg);
}

.accordion-item-body {
  display: none;
  height: 200px;
  padding: 20px;
  border: 1px solid rgb(172, 172, 172);
  border-radius: 25px;
}
.accordion-item-head.active + .accordion-item-body {
  display: block !important;
}
</style>
