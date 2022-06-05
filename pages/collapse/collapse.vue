<template>
	<view>
<!-- 		<uni-collapse>
			<uni-collapse-item title="默认开启" :open="true">
				<text>折叠内容</text>
			</uni-collapse-item>
			<uni-collapse-item title="折叠内容">
					<text>折叠内容</text>
			</uni-collapse-item>
			<uni-collapse-item title="禁用状态" disabled>
				<text>折叠内容</text>
			</uni-collapse-item>
		</uni-collapse> -->
		
<!-- 		<uni-collapse accordion>
			<uni-collapse-item title="手风琴效果">
				<text>折叠内容</text>
			</uni-collapse-item>
			<uni-collapse-item title="手风琴效果">
					<text>折叠内容</text>
			</uni-collapse-item>
			<uni-collapse-item title="禁用状态" disabled>
				<text>折叠内容</text>
			</uni-collapse-item>
		</uni-collapse> -->
		
		<uni-collapse>
			<uni-collapse-item title="标题文字"
				thumb="https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png">
				<view class="content">
					<text class="text">折叠内容主体，可自定义内容及样式</text>
				</view>
			</uni-collapse-item>
			<uni-collapse-item title="手风琴效果">
					<text>折叠内容</text>
			</uni-collapse-item>
			<uni-collapse-item title="禁用状态" disabled>
				<text>折叠内容</text>
			</uni-collapse-item>
		</uni-collapse>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
