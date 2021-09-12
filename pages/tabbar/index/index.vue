<template>
	<view class="content">
		<!-- 自定义导航栏 -->
		<navbar></navbar>
		<!--自定义 tab  -->
		<tab :list="tabList"></tab>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				tabList: [],
			}
		},
		onLoad() {
			this.getLabel();
		},
		methods: {
			getLabel() {
				// 调用云函数方法
				this.$api.get_label({
					name: 'get_label'
				}).then((res) => {
					const {
						data
					} = res;
					this.tabList = data;
					console.log("tabList",this.tabList)
				})

			}
		}
	}
</script>

<style lang="scss">
</style>
