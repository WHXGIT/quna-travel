<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <home-recommend></home-recommend>
<<<<<<< HEAD
=======
      <home-weekend></home-weekend>
>>>>>>> index-recommend
     </div>
  </div>
</template>
<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
<<<<<<< HEAD
  import HomeRecommend from './components/Recommend.vue'
=======
  import HomeRecommend from './components/Recommend'
  import HomeWeekend from './components/Weekend'
>>>>>>> index-recommend
  export default {
    name: 'Home',
    data() {
      return {}
    },
    components: {
      HomeIcons,
      HomeSwiper,
      HomeHeader,
<<<<<<< HEAD
      HomeRecommend
=======
      HomeRecommend,
      HomeWeekend
>>>>>>> index-recommend
    }
  }
</script>
<style scoped lang="scss">

</style>
