<template>
	<view class="container">
		<uni-badge size="small" :text="1" absolute="rightTop" type="primary"
		:offset="[10, 10]"><button type="default">通知</button></uni-badge>
		<!-- 
		<uni-badge text="1"></uni-badge>

		<uni-badge text="2" type="purple" @click="bindClick"></uni-badge>

		<uni-badge text="3" type="primary" :inverted="false"></uni-badge> -->
		
		
	</view>
</template>

<script>
export default {
	data() {
		return {
			href: 'https://uniapp.dcloud.io/component/README?id=uniui'
		};
	},
	methods: {}
};
</script>

<style>
.container {
	padding: 20px;
	font-size: 14px;
	line-height: 24px;
}
</style>
