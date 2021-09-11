<template>
	<view class="content">
		<!-- 自定义导航栏 -->
		<navbar></navbar>
		<view v-for="item in 100">{{item}}个内容</view>
	</view>
</template>

<script>
	// easyCom components/组件名/组件名.vue 局部引入 不需要import+components
	// import navbar from '@/components/navbar/navbar.vue'
	export default {
		// components: {
		// 	navbar
		// },
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
