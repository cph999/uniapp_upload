<template>
	<view>
		<uni-card title="基础卡片" sub-title="副标题" extra="额外信息" thumbnail="/static/c1.png">
			<text>这是一个带头像和双标题的基础卡片，此示例展示了一个完整的卡片。</text>
		</uni-card>
		<uni-card cover="https://vkceyugu.cdn.bspapp.com/VKCEYUGU-dc-site/460d46d0-4fcc-11eb-8ff1-d5dcf8779628.png"
	>
			<text>这是一个带封面和操作栏的卡片示例，此示例展示了封面插槽和操作栏插槽的用法。</text>
			<template v-slot:actions>
				<view class="card-actions">
					<view class="card-actions-item" @click="actionsClick('分享')">
						<uni-icons type="pengyouquan" size="18" color="#999"></uni-icons>
						<text class="card-actions-item-text">分享</text>
					</view>
					<view class="card-actions-item" @click="actionsClick('点赞')">
						<uni-icons type="heart" size="18" color="#999"></uni-icons>
						<text class="card-actions-item-text">点赞</text>
					</view>
					<view class="card-actions-item" @click="actionsClick('评论')">
						<uni-icons type="chatbubble" size="18" color="#999"></uni-icons>
						<text class="card-actions-item-text">评论</text>
					</view>
				</view>
			</template>
		</uni-card>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	methods: {
		actionsClick(opreation) {
			if (opreation === '点赞') {
				console.log("thumb up");
			} else if (opreation === '评论') {
				console.log("comment");
			} else {
				console.log("share");
			}
		}
	}
};
</script>

<style></style>
