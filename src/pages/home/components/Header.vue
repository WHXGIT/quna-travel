<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
     <span class="iconfont">&#xe632;</span> 输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市<span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {}
    }
  }
</script>
<style scoped lang="scss">
  @import '~styles/theme.scss';
  .header {
    background: $bgColor;

    display: flex;
    color: #fff;
    line-height: 2.86rem;
    .header-left {
      width: 2.64rem;
      float: left;
      .back-icon{
        text-align: center;
        font-size: 1.1rem;
      }
    }
    .header-input {
      margin-top: .4rem;
      flex: 1;
      border-radius: .2rem;
      background: #fff;
      line-height: 2.06rem;
      height: 2.06rem;
      margin-left: .2rem;
      color: #ccc;
      padding-left: 1rem;
    }
    .header-right {
      width: 3.64rem;
      float: right;
      text-align: center;
    }

  }
</style>
