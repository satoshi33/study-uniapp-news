<template>
	<view class="content">
		<!-- 自定义导航栏 -->
		<navbar></navbar>
		<!--自定义 tab  -->
		<tab></tab>
		<view v-for="item in 100">{{item}}个内容</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
</style>
