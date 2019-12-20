<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view>
			<text class="title">{{title}}</text>
		</view>
		<view :data-length="list.length">{{list.length}}</view>
		<view v-for="(item, index) in list" :key="index" :data-length="list.length">{{index}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				listTest: []
			}
		},
		computed: {
			list() {
				return this.listTest
			}
		},
		onLoad() {
			setTimeout(() => {
				this.listTest = [1,2,3]
			}, 2000)
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
