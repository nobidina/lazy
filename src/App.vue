<template>
  <main id="app">
    <page-header />
    <hero />
    <gallery />
    <how />
    <features />
    <download />
    <page-footer />
  </main>
</template>

<script>
import Download from './components/Download.vue'
import Features from './components/Features.vue'
import Gallery from './components/Gallery.vue'
import Hero from './components/Hero.vue'
import How from './components/How.vue'
import PageFooter from './components/PageFooter.vue'
import PageHeader from './components/PageHeader.vue'

export default {
  name: 'App',
  components: {
    Download,
    Features,
    Gallery,
    Hero,
    How,
    PageFooter,
    PageHeader,
  }
}
</script>

<style lang="less">
@import "less/variables.less";
@import "less/reset.less";

html, body {
  margin: 0;
  height: 100%;
  min-height: 100%;
}

#app {
  min-height: 100%;
  font-family: @font-family-text;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 18px;
  line-height: 135%;
  color: @font-color;
}
</style>
