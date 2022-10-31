<template>
  <section class="features">
    <ul class="features__list">
      <li class="features__item" v-for="item in features" :key="item.id">
        <div class="features__content">
          <h2 class="features__title">
            {{item.title}}
          </h2>
          <p class="features__text">
            {{item.text}}
          </p>
        </div>
        <div class="features__img-wrap">
          <div class="features__shadow features__shadow--100"></div>
          <div class="features__shadow features__shadow--80"></div>
          <div class="features__shadow features__shadow--60"></div>
          <div class="features__shadow features__shadow--40"></div>
          <div class="features__shadow features__shadow--20"></div>
          <div class="features__shadow features__shadow--10"></div>
          <div class="features__shadow features__shadow--5"></div>
          <div class="features__shadow features__shadow--2"></div>
          <img class="features__img" :src="item.img1x" :srcset="item.imag2x" :alt="item.title" />
        </div>
      </li>
    </ul>
  </section>
</template>

<script>
import feature_1_1x from "../assets/feature-1@1x.jpg";
import feature_1_2x from "../assets/feature-1@2x.jpg";
import feature_2_1x from "../assets/feature-2@1x.jpg";
import feature_2_2x from "../assets/feature-2@2x.jpg";
import feature_3_1x from "../assets/feature-3@1x.jpg";
import feature_3_2x from "../assets/feature-3@2x.jpg";
import feature_4_1x from "../assets/feature-4@1x.jpg";
import feature_4_2x from "../assets/feature-4@2x.jpg";
import feature_5_1x from "../assets/feature-5@1x.jpg";
import feature_5_2x from "../assets/feature-5@2x.jpg";

export default {
  name: 'Features',
  data: () => ({
    features: [
      {
        id: 1,
        title: 'All in one',
        text: `See what’s on in your 🏙 city, book activities,presale/buy/resale tickets, store all reservations in the app, create your own events`,
        img1x: feature_1_1x,
        imag2x: feature_1_2x,
      },
      {
        id: 2,
        title: 'CustomizeD for you',
        text: 'LAZY feed can be customized by your preferences so you don/’t need to wade through tonnes 👀 of unwanted activities',
        img1x: feature_2_1x,
        imag2x: feature_2_2x,
      },
      {
        id: 3,
        title: 'Subscribe to what you like ',
        text: 'Follow artists, venues or friends to see their recommendations, collections, liked ❤️ events and places',
        img1x: feature_3_1x,
        imag2x: feature_3_2x,
      },
      {
        id: 4,
        title: 'Random activities',
        text: 'Don’t know what you want? 🤔Lazy can surprise you with random activities',
        img1x: feature_4_1x,
        imag2x: feature_4_2x,
      },
      {
        id: 5,
        title: 'Add your own events',
        text: 'Still didn’t found perfect activity? Not a problem. Create 🪄 one yourself!',
        img1x: feature_5_1x,
        imag2x: feature_5_2x,
      },
    ],
  }),
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
  .features {
    min-height: 100%;

    &:hover {

      .features__img {
        animation: app-screen 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--100 {
        animation: shadow--100 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--80 {
        animation: shadow--80 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--60 {
        animation: shadow--60 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--40 {
        animation: shadow--40 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--20 {
        animation: shadow--20 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--10 {
        animation: shadow--10 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__shadow--5 {
        animation: shadow--5 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__img {
        animation: app-screen--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--100 {
        animation: shadow--100--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--80 {
        animation: shadow--80--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--60 {
        animation: shadow--60--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--40 {
        animation: shadow--40--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--20 {
        animation: shadow--20--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--10 {
        animation: shadow--10--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }

      .features__item:nth-child(even) .features__shadow--5 {
        animation: shadow--5--reverse 0.5s linear;
        animation-fill-mode: forwards;
      }
    }

    &__list {
      max-width: 1108px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding-top: 148px;
      padding-bottom: 148px;
    }

    &__item {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-bottom: 120px;

      &:nth-child(even) {
        .features__img-wrap {
          order: -1;
        }

        .features__shadow {
          left: 0;
          right: none;
        }
        .features__img {
          left: 0;
          right: none;
        }
      }

      &:nth-child(2) {
        .features__shadow {
          background-color: @cream;
        }
      }

      &:nth-child(3) {
        .features__shadow {
          background-color: @green;
        }
      }

      &:nth-child(4) {
        .features__shadow {
          background-color: @blue;
        }
      }

      &:nth-child(5) {
        .features__shadow {
          background-color: @cream;
        }
      }
    }

    &__content {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 538px;
      margin-right: 32px;
    }

    &__title {
      width: 290px;
      margin-bottom: 40px;
      text-align: center;
      text-transform: uppercase;
      font-family: @font-family-title;
      font-size: 50px;
      line-height: 130%;
    }

    &__text {
      width: 290px;
      text-align: center;
    }

    &__img-wrap {
      position: relative;
      width: 538px;
      height: 614px;
    }

    &__shadow {
      position: absolute;
      top: 0;
      right: 0;
      box-sizing: border-box;
      width: 253px;
      height: 548px;
      border: 4px solid @black;
      border-radius: 32px;
      background: @red;

      &--100 {
        opacity: 1;
        z-index: 8;
      }

      &--80 {
        opacity: 0.8;
        z-index: 7;
      }

      &--60 {
        opacity: 0.6;
        z-index: 6;
      }

      &--40 {
        opacity: 0.4;
        z-index: 5;
      }

      &--20 {
        opacity: 0.2;
        z-index: 4;
      }

      &--10 {
        opacity: 0.1;
        z-index: 3;
      }

      &--5 {
        opacity: 0.05;
        z-index: 1;
      }

      &--2 {
        opacity: 0.02;
        z-index: 0;
      }
    }

    &__img {
      position: absolute;
      top: 0;
      right: 0;
      z-index: 9;
      display: block;
      width: 253px;
      height: 548px;
      border-radius: 34px;
    }
  }

  @keyframes app-screen {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 64px;
      right: 224px;
    }
  }

  @keyframes shadow--100 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 56px;
      right: 196px;
    }
  }

  @keyframes shadow--80 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 48px;
      right: 168px;
    }
  }

  @keyframes shadow--60 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 40px;
      right: 140px;
    }
  }

  @keyframes shadow--40 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 32px;
      right: 112px;
    }
  }

  @keyframes shadow--20 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 24px;
      right: 84px;
    }
  }

  @keyframes shadow--10 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 16px;
      right: 56px;
    }
  }

  @keyframes shadow--5 {
    0% {
      top: 0;
      right: 0;
    }
    100% {
      top: 8px;
      right: 28px;
    }
  }

  @keyframes app-screen--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 64px;
      left: 224px;
    }
  }

  @keyframes shadow--100--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 56px;
      left: 196px;
    }
  }

  @keyframes shadow--80--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 48px;
      left: 168px;
    }
  }

  @keyframes shadow--60--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 40px;
      left: 140px;
    }
  }

  @keyframes shadow--40--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 32px;
      left: 112px;
    }
  }

  @keyframes shadow--20--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 24px;
      left: 84px;
    }
  }

  @keyframes shadow--10--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 16px;
      left: 56px;
    }
  }

  @keyframes shadow--5--reverse {
    0% {
      top: 0;
      left: 0;
    }
    100% {
      top: 8px;
      left: 28px;
    }
  }
</style>
