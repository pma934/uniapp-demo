<template>
	<view class="content">
		<navbar :isHome="true" titleText="首页"/>
		<button style="margin-top: 130rpx;" @click="navigateTo">跳转</button>
	</view>
</template>

<script setup>
	import { ref, reactive, computed } from 'vue'
	const data = ref('动态组件')
	const changeData = (val) => {
		data.value = val
	}
	const navigateTo = () => {
		uni.navigateTo({
			url:'/pages/search/index'
		})
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
