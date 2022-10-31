<template>
  <div class="carousel">
    <ul class="carousel__list">
      <li class="carousel__item" v-for="item in memories" :key="item.id">
        <svg class="carousel__pin" width="16" height="84" viewBox="0 0 16 84" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M0 81.0841V1.26758H8.31533V81.0841H0Z" fill="#DFC7A0"/>
          <path d="M0.855553 82.8758L6.56876 0.467549L15.9098 3.1542L10.5115 83.2734L0.855553 82.8758Z" fill="#FFEBD3"/>
          <path d="M9.21436 47.7075L1.57324 47.0413V49.4842L9.21436 50.2615V47.7075Z" fill="#DFC7A0"/>
        </svg>
        <div class="carousel__inner">
          <img class="carousel__img" :src="item.img_1x" :srcSet="item.img_2x" :alt="item.title" />
          <h3 class="carousel__title">
            {{item.title}}
          </h3>
          <p class="carousel__date">
            {{item.date}}
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
import gallery_1_1x from "../assets/gallery-1@1x.jpg";
import gallery_1_2x from "../assets/gallery-1@2x.jpg";
import gallery_2_1x from "../assets/gallery-2@1x.jpg";
import gallery_2_2x from "../assets/gallery-2@2x.jpg";
import gallery_3_1x from "../assets/gallery-3@1x.jpg";
import gallery_3_2x from "../assets/gallery-3@2x.jpg";
import gallery_4_1x from "../assets/gallery-4@1x.jpg";
import gallery_4_2x from "../assets/gallery-4@2x.jpg";
import gallery_5_1x from "../assets/gallery-5@1x.jpg";
import gallery_5_2x from "../assets/gallery-5@2x.jpg";
import gallery_6_1x from "../assets/gallery-6@1x.jpg";
import gallery_6_2x from "../assets/gallery-6@2x.jpg";


export default {
  name: 'Carousel',
  data: () => ({
    memories: [
      {
        id: 1,
        img_1x: gallery_1_1x,
        img_2x: gallery_1_2x,
        title: 'Design local party',
        date: '02.08.2022',
      },
      {
        id: 2,
        img_1x: gallery_2_1x,
        img_2x: gallery_2_2x,
        title: 'Ready for yoga lesson',
        date: '15.06.2021',
      },
      {
        id: 3,
        img_1x: gallery_3_1x,
        img_2x: gallery_3_2x,
        title: 'Discover art',
        date: '20.06.2022',
      },
      {
        id: 4,
        img_1x: gallery_4_1x,
        img_2x: gallery_4_2x,
        title: 'Meet new friends',
        date: '07.02.2019',
      },
      {
        id: 5,
        img_1x: gallery_5_1x,
        img_2x: gallery_5_2x,
        title: 'Open to adventures',
        date: '15.05.2021',
      },
      {
        id: 6,
        img_1x: gallery_6_1x,
        img_2x: gallery_6_2x,
        title: 'Feel the music',
        date: '28.08.2018',
      },
      {
        id: 7,
        img_1x: gallery_1_1x,
        img_2x: gallery_1_2x,
        title: 'Design local party',
        date: '02.08.2022',
      },
      {
        id: 8,
        img_1x: gallery_2_1x,
        img_2x: gallery_2_2x,
        title: 'Ready for yoga lesson',
        date: '15.06.2021',
      },
      {
        id: 9,
        img_1x: gallery_3_1x,
        img_2x: gallery_3_2x,
        title: 'Discover art',
        date: '20.06.2022',
      },
      {
        id: 10,
        img_1x: gallery_4_1x,
        img_2x: gallery_4_2x,
        title: 'Meet new friends',
        date: '07.02.2019',
      },
      {
        id: 11,
        img_1x: gallery_5_1x,
        img_2x: gallery_5_2x,
        title: 'Open to adventures',
        date: '15.05.2021',
      },
      {
        id: 12,
        img_1x: gallery_6_1x,
        img_2x: gallery_6_2x,
        title: 'Feel the music',
        date: '28.08.2018',
      },
    ],
  }),
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
  .carousel {
    overflow: hidden;
    width: 100%;
    padding-bottom: 20px;
    
    &__list {
      display: flex;
      flex-direction: row;
      width: calc(335px * 12 + 352px);
      animation: train 25s linear infinite;
    }

    &__item {
      flex-shrink: 0;
      width: 335px;
      position: relative;
      margin-right: 32px;
      padding-top: 56px;

      &:nth-child(even) {
        margin-top: 20px;
      }

      &:last-child {
        margin-right: 0;
      }
    }

    &__inner {
      padding: 8px;
      border: 1px solid @grey;
      box-shadow: 10px 10px 10px rgba(43, 45, 51, 0.1);
      border-radius: 4px;
      background: @white;
    }

    &__pin {
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
    }

    &__img {
      width: 100%;
      height: auto;
      margin-bottom: 10px;
    }

    &__title {
      margin-bottom: 8px;
      text-transform: uppercase;
      font-family: @font-family-title;
      font-size: 20px;
      line-height: 130%;
    }

    &__date {
      font-size: 16px;
      line-height: 135%;
      text-align: right;
    }
  }

  @keyframes train {
    0% { 
      transform: translateX(0);
    }
    100% { 
      transform: translateX(calc(-335px * 6 - 192px));
    }
  }
</style>
