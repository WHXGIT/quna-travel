<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item" v-for="(item, index) of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img"
               :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">{{item.buttonValue}}</button>
        </div>
      </li>
    </ul>
  </div>
</template>
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
</style>
