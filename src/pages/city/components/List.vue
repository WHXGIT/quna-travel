<template>
	<div class="list" ref="wrapper">
		<div>
			<div class="area">
				<div class="title border-topbottom">当前城市</div>
				<div class="button-list">
					<div class="button-wrapper">
						<div class="button">
							{{this.currentCtiy}}
						</div>
					</div>
				</div>
			</div>
			<div class="area">
				<div class="title border-topbottom">热门城市</div>
				<div class="button-list">
					<div class="button-wrapper" v-for="item of hotCities" :key="item.id" @click="handleCityClick(item.name)">
						<div class="button">
							{{item.name}}
						</div>
					</div>
				</div>
			</div>
			<div class="area" v-for="(item, key) of cities" :key="key" :ref="key">
				<div class="title border-topbottom">{{key}}</div>
				<ul class="item-list">
					<li class="item b-1px-t:before" v-for="innerItem of item" :key="innerItem.id" @click="handleCityClick(innerItem.name)">
						{{innerItem.name}}
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
import Bscroll from 'better-scroll'
import { mapState, mapMutations } from 'vuex'
export default {
	name: "CityList",
	props: {
		cities: Object,
		hotCities: Array,
		letter: String
	},
	data() {
		return {

		}
	},
	watch: {
		letter() {
			if (this.letter) {
				const element = this.$refs[this.letter][0];
				this.scroll.scrollToElement(element);
			}
		}
	},
	computed: {
		...mapState({
			currentCtiy: 'city'
		})
	},
	methods: {
		handleCityClick(city) {
			this.changeCity(city);
			this.$router.push('/')
		},
		...mapMutations(['changeCity'])
	},
	mounted() {
		this.scroll = new Bscroll(this.$refs.wrapper)
	},
	components: {

	}
}
</script>

<style scoped lang="scss">
@import '~styles/theme.scss';
@import '~styles/border';
.border-topbottom {
	&:before {
		border-color: #ccc;
	}
	&:after {
		border-color: #ccc;
	}
}
.border-bottom {
	&:before {
		border-color: #ccc;
	}
}
.list {
	position: absolute;
	overflow: hidden;
	top: 4.8rem;
	bottom: 0;
	left: 0;
	right: 0;
	.title {
		line-height: 2rem;
		background: #eee;
		padding-left: 0.8rem;
		color: #666;
		font-size: 1rem;
	}
	.button-list {
		padding: 0.4rem 2.4rem 0.4rem 0.4rem;
		overflow: hidden;
		.button-wrapper {
			float: left;
			width: 33.33%;
			.button {
				padding: 0.2rem 0;
				margin: 0.4rem;
				text-align: center;
				border: 0.08rem solid #ccc;
				border-radius: 0.24rem;
			}
		}
	}
	.item-list {
		.item {
			line-height: 2.3rem;
			padding-left: 0.8rem;
			border-bottom: 1px;
			border-bottom-style: ridge;
		}
	}
}
</style>
