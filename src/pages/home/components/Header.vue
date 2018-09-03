<template>
	<div class="header">
		<div class="header-left">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
			<span class="iconfont">&#xe632;</span> 输入城市/景点/游玩主题
		</div>
		<router-link to="/city">
			<div class="header-right">
				{{this.city}}
				<span class="iconfont">&#xe6aa;</span>
			</div>
		</router-link>
	</div>
</template>
<script>
import { mapState } from 'vuex'
export default {
	data() {
		return {}
	},
	computed: {
		...mapState(['city'])
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
		.back-icon {
			text-align: center;
			font-size: 1.1rem;
		}
	}
	.header-input {
		margin-top: 0.4rem;
		flex: 1;
		border-radius: 0.2rem;
		background: #fff;
		line-height: 2.06rem;
		height: 2.06rem;
		margin-left: 0.2rem;
		color: #ccc;
		padding-left: 1rem;
	}
	.header-right {
		min-width: 3.04rem;
		padding: 0.3rem;
		float: right;
		color: #ffffff;
		text-align: center;
	}
}
</style>
