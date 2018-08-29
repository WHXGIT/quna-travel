<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <home-recommend></home-recommend>
      <home-weekend></home-weekend>
    </div>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  data() {
    return {}
  },
  components: {
    HomeIcons,
    HomeSwiper,
    HomeHeader,
    HomeRecommend,
    HomeWeekend,
    axios
  },
  methods: {
    getHomeInfo() {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSuccess)
    },
    getHomeInfoSuccess(res) {
        console.log(res.data.name);
    }
  },
  mounted() {
    this.getHomeInfo();
  }
}
</script>
<style scoped lang="scss">
</style>
