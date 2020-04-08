<template>
  <div class="container">
    <div class="sessions">
      <div class="sessions__title">{{ title }}</div>

      <div class="sessions__inner">
        <div class="card" v-for="(value, key) in sessions" :key="key">
          <template>
            <div class="card__header">
              <div class="card__header-title">{{ value.title }}</div>
              <div class="card__header-item card__header-item--duration">
                Duration: {{ value.duration }}
              </div>
              <div class="card__header-item card__header-item--date">
                Date: {{ value.date }}
              </div>
              <a class="card__header-item card__header-item--video" href
                >View video</a
              >
            </div>
            <div class="card__content">
              <div class="card__img">
                <img :src="getPic(value.user_id)" :alt="value.user_id" />
                <img
                  style="padding-left: 20px"
                  v-if="value.user2_id"
                  :src="getPic(value.user2_id)"
                  :alt="value.user2_id"
                />
              </div>
              <div class="card__text">{{ value.text }}</div>
            </div>
          </template>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sessions",
  data: () => ({
    title: "Sessions",
    sessions: {
      1: {
        user_id: 1,
        title: "First Sessions",
        duration: "6 hour",
        date: "November 5",
        text: `In the first session, we will consider design thinking and its understanding as well as
               different models of design thinking and the design process, and we will better remember
               this process with various examples. We will also discuss problem solving techniques together
               and understand the concept of user experience and usability.`
      },
      2: {
        user_id: 2,
        title: "Second Sessions",
        duration: "6 hour",
        date: "November 7",
        text: `In the second session, we will discuss service design, first discussing “What is a service?”
               Then we practice how to create the right conditions for them in the long run to stay loyal to
               our product based on the actual needs of our audience and to create solutions that will reduce
               the hassle of the user in the short run. We are also going to create a way to measure the performance
               of our product so that we can ensure the quality of the design solution’s performance.`
      },
      3: {
        user_id: 1,
        title: "Third Sessions",
        duration: "6 hour",
        date: "November 8",
        text: `In the third session we will discuss the most important design phase, which is the initial research
               and review process. We will explore user experience research and user research methods.
               At the end of the session we will be able to build user personas as well as user scenarios and narrated user
               stories in the product.`
      },
      4: {
        user_id: 3,
        title: "Fourth Sessions",
        duration: "5 hour",
        date: "November 9",
        text: `Building experience is one of the key points in product management and design. But how does this experience
               come about? The experience is made by creating a unique feeling in the mind. In the fourth session, we will
               learn how to identify users’ behavior and motivate them as well as build stimuli to drive the minds of the
               target audience together.`
      },
      5: {
        user_id: 1,
        user2_id: 4,
        title: "Fifth Meeting",
        duration: "7 hour",
        date: "November 10",
        text: `Building experience is one of the key points in product management and design. But how does this experience
               come about? The experience is made by creating a unique feeling in the mind. In the fourth session, we will
               learn how to identify users’ behavior and motivate them as well as build stimuli to drive the minds of the
               target audience together.`
      },
      6: {
        user_id: 5,
        user2_id: 6,
        title: "Sixth Session",
        duration: "5 hour",
        date: "November 11",
        text: `Today, the world is a world of interaction, in the sixth session we understand users trying to find the
               best way to interact with them and bring the emotions, perceptions, and awareness of the users to the
               forefront. We will explore the concept of Interaction Design and also explore it in terms of user
               experience design, usability and intuitive interface design. In the second part of the sixth session,
               we go into marketing and practice the marketing strategy of digital products together, as well as
               discussing the appropriate digital marketing toolkit.`
      },
      7: {
        user_id: 7,
        title: "Seventh Session",
        duration: "5 hour",
        date: "November 12",
        text: `In the seventh session, we are in the world of product management. We will examine software companies’ structures
               as well as in-team and in-team interactions. In this session, we will look at the duties and characteristics of
               product team members as well as identify product strategies and learn about different software development
               methodologies. And finally, we’ll look at a product designer’s red line.`
      },
      8: {
        user_id: 8,
        user2_id: 9,
        title: "Eighth Session",
        duration: "6 hour",
        date: "November 13",
        text: `In this session, we will get our hands into the color, learn the basics of user interface design with colored hands,
               and learn about various interface design tools. We also explore the concepts and fundamentals of iconography and
               learn about testing the usability of icon design and finally learn the process of visualization in digital products
               from idea to implementation.`
      },
      9: {
        user_id: 8,
        user2_id: 10,
        title: "Ninth Session",
        duration: "5 hour",
        date: "November 14",
        text: `In the ninth session we will continue to immerse ourselves in the world of color and image, identifying the elements
               of the interface and learning how to properly represent the data. We also remotely team up with Moslem Ebrahimi,
               a typeface designer, and look at the typography of digital products from the perspective of someone who has had
               a lifetime of concern for typefaces and Persian fonts.`
      },
      10: {
        user_id: 8,
        title: "Tenth Session",
        duration: "6 hour",
        date: "November 15",
        text: `In the 10th session we will start with the software and together we will learn what design software capabilities
               are and what ideas can be made with them and that they are not as complex as the cockpit!`
      }
    }
  }),
  methods: {
    getPic(id) {
      return require(`../assets/images/sessions/${id}.png`);
    }
  }
};
</script>

<style lang="scss" scoped>
.sessions {
  margin-bottom: 100px;
  position: relative;

  &__title {
    width: 470px;
    height: 160px;
    margin: 110px auto 50px;
    padding: 80px 25px 0;
    font-size: 34px;
    font-weight: bold;
    line-height: 46px;
    text-align: center;
    background-image: url("../assets/images/Sessions.png");
    background-size: cover;
  }

  &__inner::before {
    content: "";
    display: block;
    width: 2px;
    height: 91%;
    background: #e8e8e8;
    position: absolute;
    top: 220px;
    left: 2px;
    z-index: 2;
  }

  .card {
    margin-bottom: 20px;
    padding: 0 20px;

    &__header {
      display: flex;
      align-items: center;
      height: 55px;
      padding: 0 30px;
      background: #f8f8f8;
      border-radius: 12px;
      position: relative;

      &::before {
        content: "";
        display: block;
        width: 6px;
        height: 40px;
        background: #000;
        position: absolute;
        border-radius: 6px;
        top: 50%;
        left: -20px;
        z-index: 2;
        transform: translate3d(0, -50%, 0);
      }

      &-title {
        width: 350px;
        font-size: 20px;
        font-weight: bold;
        line-height: 35px;
      }
      &-item {
        padding-right: 130px;
        padding-left: 30px;
        font-size: 19px;
        line-height: 26px;
        position: relative;

        &--duration::before {
          display: block;
          content: url("../assets/images/sessions/duration.png");
          width: 25px;
          height: 25px;
          position: absolute;
          top: 0;
          left: 0;
        }

        &--date::before {
          display: block;
          content: url("../assets/images/sessions/date.png");
          width: 25px;
          height: 25px;
          position: absolute;
          top: 0;
          left: 0;
        }

        &--video {
          color: #000;
          text-decoration: none !important;
          padding-left: 35px;
          &::before {
            display: block;
            content: url("../assets/images/sessions/video.png");
            width: 30px;
            height: 30px;
            position: absolute;
            top: -3px;
            left: 0;
          }
        }
      }
    }

    &__content {
      display: flex;
      align-items: center;
      padding: 30px 50px 50px 30px;
    }

    &__img {
      min-width: 350px !important;
    }

    &__text {
      font-size: 16px;
      line-height: 34px;
      padding-right: 50px;
    }
  }
}
</style>
