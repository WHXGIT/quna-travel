<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="(item, index) of page" :key="item.id">
          <div class="icons-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icons-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>
</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    iconList: Array
  },
  data() {
    return {
      
    }
  },
  computed: {
    pages() {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style scoped lang="scss">
@import '~styles/theme.scss';
@import '~styles/maxins.scss';
.icons >>> .swiper-container {
	height: 0;
	padding-bottom: 50%;
}
.icon {
	width: 25%;
	float: left;
	padding-bottom: 25%;
	height: 0;
	margin-top: 0.2rem;
	overflow: hidden;
	position: relative;
	.icons-desc {
		position: absolute;
		left: 0;
		right: 0;
		bottom: 4px;
		height: 1.44rem;
		bottom: 0.5rem;
		height: 1rem;
		line-height: 1.1rem;
		height: 1.1rem;
		line-height: 1.1rem;
		color: $darkTextColor;
		text-align: center;
		@include ellipsis;
	}
	.icons-img {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0.44rem;
		box-sizing: border-box;
		padding: 0.1rem;
		.icon-img-content {
			height: 75%;
			display: block;
			margin: 0 auto;
		}
	}
}
</style>
