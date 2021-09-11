<template>
	<view class="navbar">
		<view class="navbar-fixed">
			<view class="navbar-search">
				<view class="navbar-search_icon"></view>
				<view class="navbar-search_text">uni-app、vue</view>
			</view>
		</view>
		<!-- 上方navbar-fixed固定position: fixed后，会遮挡navbar兄弟组件内容 -->
		<view style="height: 45px;"></view>
	</view>
</template>

<script>
	export default {
		name: "navbar",
		data() {
			return {

			};
		}
	}
</script>

<style lang="scss">
	.navbar {
		.navbar-fixed {
			position: fixed;
			top: 0;
			left: 0;
			z-index: 99;
			
			width: 100%;
			background-color: $mk-base-color;
			
			display: flex;
			justify-content: center;
			align-items: center;
			padding: 0 15px;
			height: 45px;
			box-sizing: border-box;

			.navbar-search {
				display: flex;
				align-items: center;
				padding: 0 10px;
				width: 100%;
				height: 30px;
				border-radius: 30px;
				background-color: #fff;

				.navbar-search_icon {
					width: 10px;
					height: 10px;
					border: 1px red solid;
					margin-right: 10px;
				}

				.navbar-search_text {
					width: 100%;
					font-size: 14px;
					color: #999;
				}

			}
		}
	}
</style>
