<template>
  <div>
    <div>
      <home-header></home-header>
      <home-swiper :list="swiperList"></home-swiper>
      <home-icons :icon-list="iconList"></home-icons>
      <home-recommend :recommend-list="recommendList"></home-recommend>
      <home-weekend :weekend-list="weekendList"></home-weekend>
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
import { mapState } from 'vuex'
export default {
  name: 'Home',
  data() {
    return {
      lastCity: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  computed: {
  	...mapState(['city'])
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
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSuccess)
    },
    getHomeInfoSuccess(res) {
      const data = res.data.data;
      this.swiperList = data.swiperList;
      this.iconList = data.iconList;
      this.recommendList = data.recommendList;
      this.weekendList = data.weekendList;
    },

  },
  mounted() {
    this.getHomeInfo();
    this.lastCity = this.city
  },
  activated() {
    if (this.lastCity !== this.city) {
      this.lastCity = this.city
      this.getHomeInfo
    }
  }
}
</script>
<style scoped lang="scss">
</style>
