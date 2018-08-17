<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>

    </div>
  </div>
</template>
<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'

  export default {
    name: 'Home',
    data() {
      return {}
    },
    components: {
      HomeSwiper,
      HomeHeader
    }
  }
</script>
<style scoped lang="scss">

</style>
