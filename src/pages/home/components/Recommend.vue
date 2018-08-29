<template>
  <div>
<<<<<<< HEAD
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item, index) of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img"
               :src="item.imgUrl">
=======
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item,index) of recommendList" :key=item.id>
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
>>>>>>> index-recommend
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
<<<<<<< HEAD
          <button class="item-button">{{item.buttonValue}}</button>
=======
          <button class="item-button">查看详情</button>
>>>>>>> index-recommend
        </div>
      </li>
    </ul>
  </div>
</template>
<<<<<<< HEAD
<script>
  export default {
    name: 'HomeRecommend',
    data() {
      return {
        recommendList: [
          {
            id: '0001',
            imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
            title: '武隆天坑地缝国家地质公园',
            desc: '酉阳桃花源',
            buttonValue: '查看详情'
          },
          {
            id: '0001',
            imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
            title: '武隆天坑地缝国家地质公园',
            desc: '酉阳桃花源',
            buttonValue: '查看详情'
          },
          {
            id: '0001',
            imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
            title: '武隆天坑地缝国家地质公园',
            desc: '酉阳桃花源',
            buttonValue: '查看详情'
          }]
      }
    }
  }
</script>
<style scoped lang="scss">
  @import "~styles/maxins.scss";

  .recommend-title {
    background: #eeeeee;
    margin-top: .5rem;
    line-height: 1.2rem;
    text-indent: .5rem;
  }

  .item {
    overflow: hidden;
    display: flex;
    height: 6rem;
    .item-img {
      width: 5.7rem;
      height: 5.7rem;
      padding: .2rem;
    }
    .item-info {
      flex: 1;
      padding: .2rem;
      min-width: 0;
      .item-title {
        line-height: 2rem;
        font-size: 1.5rem;
        @include ellipsis;
      }
      .item-desc {
        line-height: 1.8rem;
        color: #cccccc;
        @include ellipsis;
      }
      .item-button {
        line-height: 1.8rem;
        margin-top: 0.5rem;
        background: #ff9300;
        padding: 0 1.5rem;
        border-radius: .2rem;
        color: #ffffff;
        border: 0;
      }
    }
  }
=======

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
      recommendList: [
        {
          id:'0001',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
          desc: '武隆天坑地缝国家地质公园',
          title: '武隆天坑地缝国家地质公园'
        },
        {
          id:'0002',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
          desc: '武隆天坑地缝国家地质公园',
          title: '武隆天坑地缝国家地质公园'
        },
        {
          id:'0003',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
          desc: '武隆天坑地缝国家地质公园',
          title: '武隆天坑地缝国家地质公园'
        },
        {
          id:'0004',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/be/be4802e10f3b3107.water.jpg_200x200_0e98aabe.jpg',
          desc: '武隆天坑地缝国家地质公园',
          title: '武隆天坑地缝国家地质公园'
        },
      ]
    }
  },
  components: {

  }
}
</script>

<style scoped lang="scss">
@import "~styles/maxins.scss";

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
      color:#ffffff;
      border: 0;
			border-radius: 0.2rem;
		}
	}
}
>>>>>>> index-recommend
</style>
