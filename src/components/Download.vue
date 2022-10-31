<template>
  <section class="download">
    <h2 class="download__title">
      Download Lazy
    </h2>
    <div class="download__code">
      <img class="download__img" :src="img1x" :srcSet="img2x" alt="qrcode" />
    </div>
  </section>
</template>

<script>
import img_1x from "../assets/qrcode@1x.png"
import img_2x from "../assets/qrcode@2x.png"

export default {
  name: 'Download',
  data: () => ({
    img1x: img_1x,
    img2x: img_2x,
  }),
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
  .download {
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

    &__inner {
      max-width: 1108px;
      margin: 0 auto;
      display: flex;
      flex-direction: row;
      justify-content: center;
      padding-top: 90px;
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

    &__code {
      background: #FFEBD3;
      mix-blend-mode: lighten;
    }

    &__img {
      display: block;
      width: 320px;
      height: 320px;
      mix-blend-mode: multiply;
    }
  }
</style>
