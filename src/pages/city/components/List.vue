<template>
  <div class="list">
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">
            北京
          </div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">
            北京
          </div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <ul class="item-list">
        <li class="item b-1px-t:before">阿拉尔</li>
        <li class="item b-1px-t:before">阿拉尔</li>
        <li class="item b-1px-t:before">阿拉尔</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "CityList",
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
		}
	}
}
</style>
