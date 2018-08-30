<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item" v-for="(item,index) of recommendList" :key=item.id>
        <div class="item-img-wrapper">
          <div class="">
            <img class="item-img" :src="item.imgUrl">
          </div>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>      
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeWeekend",
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
.item-img-wrapper {
  height: 0;
  overflow: hidden;
  padding-bottom: 33.7%;
}
.item-img {
	width: 100%;
}
.item-info {
	padding: 0.1rem;
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
}
</style>
