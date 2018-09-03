<template>
	<div>
		<div class="search">
			<input v-model="keyWord" class="search-input" type="text" placeholder="输入城市名或拼音">
		</div>
		<div class="search-content" ref="searchContent" v-show="isShow">
			<ul>
				<li class="search-item border-bottom" 
				v-for="item of list" :key="item.id" 
				@click='handleCityClick(item.name)'
				>
				{{item.name}}
				</li>
				<li class="search-item border-bottom" v-show="hasNoData">没有找到匹配数据</li>
			</ul>
		</div>
	</div>
</template>

<script>
import Bscroll from 'better-scroll'
import { mapState, mapMutations } from 'vuex'
export default {
	name: "CitySearch",
	props: {
		cities: Object
	},
	data() {
		return {
			keyWord: '',
			list: [],
			timer: null,
			isShow: false
		}
	},
	watch: {
		keyWord() {
			this.isShow = true;
			if (this.timer) {
				clearTimeout(this.timer);
			}
			if (!this.keyWord) {
				this.list = []
				return
			}
			this.timer = setTimeout(() => {
				const result = [];
				for (let i in this.cities) {
					this.cities[i].forEach(element => {
						if (element.spell.indexOf(this.keyWord) > -1 || element.name.indexOf(this.keyWord) > -1) {
							result.push(element);
						}
					});
				}
				this.list = result;
			}, 100);
		}
	},
	computed: {
		hasNoData() {
			return !this.list.length;
		}
	},
	methods: {
		handleCityClick(city) {
			this.changeCity(city);
			this.$router.push('/')
		},
		...mapMutations(['changeCity'])
	},
	mounted() {
		this.scroll = new Bscroll(this.$refs.searchContent)
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
.search-content {
	z-index: 1;
	overflow: hidden;
	position: absolute;
	top: 5rem;
	bottom: 0;
	left: 0;
	right: 0;
	background: #eee;
	.search-item： {
		line-height: 2.4rem;
		padding-left: 0.8rem;
		color: #666666;
		background: #fff;
	}
}
</style>
