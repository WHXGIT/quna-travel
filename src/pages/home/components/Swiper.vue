<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="(item, index) in swiperImgUrlList" :key="item.id">
        <img class="spiper-img" :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
  export default {
    name: 'HomeSwiper',
    data() {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop: true
        },
        swiperImgUrlList: [
          {id: '0001', imgUrl: '/static/swiper1.jpg'},
          {id: '0002', imgUrl: '/static/swiper2.jpg'},
          {id: '0003', imgUrl: '/static/swiper3.jpg'}
        ]
      }
    }
  }
</script>
<style scoped lang="scss">
  .swiper {
    width: 100%;
    overflow: hidden;
    height: 0;
    padding-bottom: 8rem;
    background: #eee;
    .spiper-img {
      height: 8rem;
      width: 100%;
    }
  }
</style>
