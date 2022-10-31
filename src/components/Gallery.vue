<template>
  <section class="gallery">
    <carousel />
  </section>
</template>

<script>
import Carousel from './Carousel.vue'

export default {
  name: 'Gallery',
  components: {
    Carousel,
  }
}
</script>

<style scoped lang="less">
  @import "../less/variables.less";
  .gallery {
    min-height: 100%;
    padding-top: 58px;
    padding-bottom: 68px;
  }
</style>
