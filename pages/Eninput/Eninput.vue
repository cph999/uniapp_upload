<template>
	<view>
		<uni-easyinput v-model="value" placeholder="请输入内容"
		prefixIcon="search" ></uni-easyinput>
		
		<uni-easyinput type="idcard" autoHeight v-model="value" placeholder="请输入内容"
		></uni-easyinput>
		
		<uni-forms border>
			<uni-forms-item label="姓名">
				<uni-easyinput placeholder="请输入姓名"></uni-easyinput>
			</uni-forms-item>
			<uni-forms-item label="年龄">
				<uni-easyinput  placeholder="请输入年龄"></uni-easyinput>
			</uni-forms-item>
		</uni-forms>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				value:''
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
