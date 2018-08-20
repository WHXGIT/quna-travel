<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
     </div>
  </div>
</template>
<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
  import HomeIcons from './components/Icons'
  export default {
    name: 'Home',
    data() {
      return {}
    },
    components: {
      HomeIcons,
      HomeSwiper,
      HomeHeader
    }
  }
</script>
<style scoped lang="scss">

</style>
