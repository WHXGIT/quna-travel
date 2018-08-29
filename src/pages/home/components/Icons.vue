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
    data() {
      return {
        iconList: [
          {
            id: '0001',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            desc: '景点门票'
          },
          {
            id: '0002',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',
            desc: '景区直通车'
          },
          {
            id: '0003',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
            desc: '重庆必游'
          },
          {
            id: '0004',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
            desc: '夏日玩水'
          },
          {
            id: '0005',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
            desc: '一日游'
          },
          {
            id: '0006',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
            desc: '两江夜游'
          },
          {
            id: '0007',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
            desc: '神秘武隆'
          },
          {
            id: '0008',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/75/eca3ce656c886502.png',
            desc: '漂流'
          },
          {
            id: '0009',
            imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
            desc: '游乐场'
          }]
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
  @import "~styles/maxins.scss";

  .icons > > > .swiper-container {
    height: 1rem;
    padding-bottom: 50%;
  }

  .icon {
    width: 25%;
    float: left;
    padding-bottom: 25%;
    height: 0;
    margin-top: .5rem;
    overflow: hidden;
    position: relative;
    .icons-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 4px;
      height: 1.44rem;
      bottom: 0;
      height: 1rem;
      line-height: 1rem;
      height: 1.1rem;
      line-height: 1.44rem;
      color: $darkTextColor;
      text-align: center;
      @include ellipsis;
    }
    .icons-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: .44rem;
      box-sizing: border-box;
      padding: .1rem;
      .icon-img-content {
        height: 85%;
        display: block;
        margin: 0 auto;
      }
    }
  }
</style>
