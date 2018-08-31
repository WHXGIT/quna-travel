<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: "CitySearch",
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
.search {
	height: 2.34rem;
	padding: 0.1rem 1.2rem 0 0.4rem;
	background: #00bcd4;
	.search-input {
		width: 100%;
		height: 2rem;
		padding: 0 0.2rem;
		line-height: 2rem;
		text-align: center;
		border-radius: 0.06rem;
		color: #666666;
		border: 0;
	}
}
</style>
