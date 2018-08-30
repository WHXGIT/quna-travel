<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont header-back">
        &#xe624;
      </div>
    </router-link>
    <h1>城市选择</h1>
  </div>
</template>

<script>
export default {
  name: "CityHeader",
  data() {
    return {

    }
  },
  components: {

  }
}
</script>

<style scoped lang="scss">
@import '~styles/theme.scss';
.header {
	position: relative;
	overflow: hidden;
	height: 2.4rem;
	line-height: 2.4rem;
	text-align: center;
	font-size: 1rem;
	color: #ffffff;
	background: $bgColor;
	.header-back {
		position: absolute;
		top: 0;
		left: 1rem;
    width: 1.5rem;
    color: #FFFFFF;
	}
}
</style>
