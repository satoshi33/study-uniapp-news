<template>
	<view class="tab">
		<scroll-view class="tab-scroll" scroll-x>
			<view class="tab-scroll__box">
				<view v-for="(item, index) in list" :key="index" class="tab-scroll__item"
					:class="{active:activeIndex === index}" @click="clickTab(item, index)">{{item.name}}</view>
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
		props: {
			list: {
				type: Array,
				default () {
					return []
				}
			},
		},
		data() {
			return {
				activeIndex: 0
			};
		},
		methods: {
			clickTab(item, index) {
				this.activeIndex = index;
				this.$emit('tab', {
					data: item,
					index: index
				})
				console.log("activeIndex",item)
			},
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

					&.active {
						color: $mk-base-color;
					}
				}
			}
		}

		.tab-icons {
			position: relative;
			display: flex;
			justify-content: center;
			align-items: center;
			width: 45px;

			&::after {
				//左侧竖线
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
