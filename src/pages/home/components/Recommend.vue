<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item,index) of recommendList" :key=item.id>
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  props:{
    recommendList: Array
  },
  data() {
    return {
    }
  },
  components: {

  }
}
</script>

<style scoped lang="scss">
@import '~styles/maxins.scss';
.title {
	margin-top: 0.5rem;
	line-height: 2rem;
	background: #eeeeee;
	text-indent: 0.5rem;
}
.item {
	overflow: hidden;
	display: flex;
	height: 5.8rem;
	.item-img {
		width: 4.6rem;
		height: 4.6rem;
		padding: 0.6rem;
	}
	.item-info {
		flex: 1;
		padding: 0.1rem;
		min-width: 0;
		.item-title {
			line-height: 2rem;
			font-size: 1rem;
			@include ellipsis;
		}
		.item-desc {
			line-height: 1rem;
			color: #cccccc;
			@include ellipsis;
		}
		.item-button {
			line-height: 1.8rem;
			margin-top: 0.5rem;
			background: #ff9300;
			padding: 0 0.8rem;
			color: #ffffff;
			border: 0;
			border-radius: 0.2rem;
		}
	}
}
</style>
