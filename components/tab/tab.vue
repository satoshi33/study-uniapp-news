<template>
	<view class="tab">
		<scroll-view class="tab-scroll" scroll-x>
			<view class="tab-scroll__box">
				<view v-for="(item, index) in list" :key="index" class="tab-scroll__item">{{item.name}}零零落落零零落落</view>
			</view>
		</scroll-view>

		<view class="tab-icons">
			<uni-icons type="gear" size="26" color="#666"></uni-icons>
		</view>
	</view>
</template>

<script>
	export default {
		name: "tab",
		data() {
			return {
				list: [{
					name: "语文"
				}, {
					name: "数学"
				}, {
					name: "英语"
				}, {
					name: "数学"
				}, ]
			};
		}
	}
</script>

<style lang="scss">
	.tab {
		display: flex;
		width: 100%;
		border-bottom: 1px #f5f5f5 solid;
		background-color: #fff;


		.tab-scroll {
			flex: 1;
			overflow: hidden;
			box-sizing: border-box;
			// border: 1px red solid;

			.tab-scroll__box {
				display: flex;
				align-items: center;
				flex-wrap: nowrap;
				height: 45px;
				box-sizing: border-box;

				.tab-scroll__item {
					flex-shrink: 0; // 防止被挤压
					padding: 0 10px;
					color: #333;
					font-size: 14px;


				}

			}
		}

		.tab-icons {
			position: relative;
			display: flex;
			justify-content: center;
			align-items: center;
			width: 45px;

			&::after { //左侧竖线
				content: '';
				position: absolute;
				top: 12px;
				bottom: 12px;
				left: 0;
				width: 1px;
				background-color: #ddd;
			}
		}

	}
</style>
