<template>
	<view>
		<uni-file-picker
			v-model="imageValue"
			file-mediatype="image"
			mode="grid"
			file-extname="png,jpg"
			:limit="1"
			@progress="progress"
			@success="success"
			@fail="fail"
			@select="select"
			ref="files"
			:auto-upload="false"
		/>
		<image  v-bind:src="imageSrc"></image>
		<button @click="upload">上传文件</button>
	</view>
</template>

<script>
export default {
	data() {	
		return {
			imageValue: [],
			formData: '',
			imageSrc: 'http://chongpenghao.ltd/sad3/1231/20675e78-8d11-4dcc-905e-b01124022d42'
		};
	},
	methods: {
		// 获取上传状态
		select(e) {
			console.log('选择文件：', e);
		},
		// 获取上传进度
		progress(e) {
			console.log('上传进度：', e);
		},

		// 上传成功
		success(e) {
			console.log('上传成功');
		},

		// 上传失败
		fail(e) {
			console.log('上传失败：', e);
		},
		upload(){
			uni.chooseImage({
				success: (chooseImageRes) => {
					const tempFilePaths = chooseImageRes.tempFilePaths;
					console.log(chooseImageRes);
					uni.uploadFile({
						url: 'http://localhost:8090/oss/uploadFiles', //仅为示例，非真实的接口地址
						name: 'file',
						filePath: tempFilePaths[0],
						file: chooseImageRes.tempFiles[0],
						formData: {
							'user': 'test',
							'name':'file',	
							file: chooseImageRes.tempFiles[0],
							"storagePath": "sad3/1231",
						},
						success: (uploadFileRes) => {
							console.log(uploadFileRes.data);
							this.imageSrc = uploadFileRes.data;
						}
					});
				}
			});
		}
	}
};
</script>

<style></style>
