<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <home-recommend></home-recommend>
     </div>
  </div>
</template>
<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
  import HomeRecommend from './components/Recommend.vue'
  export default {
    name: 'Home',
    data() {
      return {}
    },
    components: {
      HomeIcons,
      HomeSwiper,
      HomeHeader,
      HomeRecommend
    }
  }
</script>
<style scoped lang="scss">

</style>
