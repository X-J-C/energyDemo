<template>
	<view class="content">
		<content_head></content_head>
		<view class="content_body">
			<uni-grid :column="2" :show-border="false" :square="false" >
				<uni-grid-item  v-for="(item ,index) in list" :index="index" :key="index">
					<view class="grid-item-box">
						<image :src="item.url" class="image" mode="aspectFill" />
						<view class="text">{{ item.title }}</view>
					</view>
				</uni-grid-item>
			</uni-grid>
		</view>
	  
	</view>
</template>

<script>
	import content_head from "../compage/head.vue"
	export default {
		components:{
			content_head:content_head
		},
		data() {
			return {
				list: [
					{
						title:"设备状态",
						url:"../../static/d1.png"
					},
					{
						title:"运行状态",
						url:"../../static/d2.png"
					}
				],
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>

/* 	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		
	} */
	
	.uni-card{
		margin:0;
		margin-top: 10px;
	}
	
.content_body{
	text-align: center;
	background-color: #fff;
	margin-top: 10px;
	padding-top: 10px;
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
	.image {
		width: 70rpx;
		height: 70rpx;
	}
	/* .text{
		font-size: 50rpx;
	} */
</style>
