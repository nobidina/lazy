<template>
  <section class="how">
    <h2 class="how__title">
      How it works
    </h2>
    <div class="how__inner">
      <ol class="how__list">
        <li class="how__item">
          <span class="how__number">
            01.
          </span>
          <span class="how__text">
            Open the app
          </span>
        </li>
        <li class="how__item">
          <span class="how__number">
            02.
          </span>
          <span class="how__text">
            Answer a couple of questions
          </span>
        </li>
        <li class="how__item">
          <span class="how__number">
            03.
          </span>
          <span class="how__text">
            Choose an activity from your personalized list
          </span>
        </li>
        <li class="how__item">
          <span class="how__number">
            04.
          </span>
          <span class="how__text">
            Book a ticket
          </span>
        </li>
        <li class="how__item">
          <span class="how__number">
            05.
          </span>
          <span class="how__text">
            Enjoy!
          </span>
        </li>
      </ol>
      <div class="how__img-wrap">
        <img class="how__img" :src="img1x" :srcSet="img2x" alt="cards from the app" />
      </div>
    </div>
  </section>
</template>

<script>
import img_1x from "../assets/how-it-works@1x.png"
import img_2x from "../assets/how-it-works@2x.png"

export default {
  name: 'How',
  data: () => ({
    img1x: img_1x,
    img2x: img_2x,
  }),
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
  .how {
    display: flex;
    flex-direction: column;
    align-items: center;
    min-height: 100%;
    padding-top: 148px;
    padding-bottom: 148px;
    background: 
      linear-gradient(
        0deg, 
        rgba(4, 44, 127, 0.2), 
        rgba(4, 44, 127, 0.2)), 
      conic-gradient(
        from 225.08deg at 50.13% 50%, 
        #000000 -61.87deg, 
        #042C7F 30deg, 
        #FD4B39 254.26deg, 
        #000000 298.12deg, 
        #042C7F 390deg);

    &:hover {
      .how__img {
        transform: scale(1);
      }
    }

    &__title {
      margin-bottom: 88px;
      text-align: center;
      text-transform: uppercase;
      font-size: 50px;
      line-height: 130%;
      font-weight: 400;
      font-family: @font-family-title;
      color: @cream;
    }

    &__inner {
      max-width: 1108px;
      margin: 0 auto;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
    }

    &__list {
      width: 443px;
      margin-right: 32px;
    }

    &__item {
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-bottom: 20px;

      &:last-child {
        margin-bottom: 0;
      }
    }

    &__number {
      display: flex;
      width: 74px;
      margin-right: 16px;
      text-transform: uppercase;
      font-family: @font-family-title;
      font-size: 50px;
      line-height: 130%;
      color: @cream;
    }

    &__text {
      font-size: 20px;
      color: @font-color-reversed;
    }

    &__img-wrap {
      width: 633px;
    }

    &__img {
      width: 100%;
      height: auto;
      transform: scale(0.8);
      transition: transform 2s;
    }
  }
</style>
