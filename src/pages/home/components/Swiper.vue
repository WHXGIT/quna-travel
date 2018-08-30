<template>
  <div class="swiper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="(item, index) in list" :key="item.id">
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
  props: {
    list: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
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
