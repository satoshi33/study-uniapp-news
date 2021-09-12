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
				uniCloud.callFunction({
					name: 'get_label'
				}).then((res) => {
					const {
						result
					} = res;
					this.tabList = result.data;
					console.log(1111,this.tabList)
				})

			}
		}
	}
</script>

<style lang="scss">
</style>
