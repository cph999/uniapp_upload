<template>
	<view>
		<uni-combox label="所在城市" :candidates="candidates" 
		placeholder="请选择所在城市" v-model="city" emptyTips="出错了"
		@input="getData()"></uni-combox>
	</view>
</template>

<script>	
	export default {
		data() {
			return {
				candidates:["河北省","北京","天津"],
				city: "河北省张家口市蔚县"
			}
		},
		methods: {
			getData(){
				
			}
		}
	}
</script>

<style>

</style>
