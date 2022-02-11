<template>
	<view class="content">
		<content_head></content_head>
		<view class="content_body">
			<uni-grid :column="4" :show-border="false" :square="false" >
				<uni-grid-item  v-for="(item ,index) in list" :index="index" :key="index">
					<view class="grid-item-box">
						<image :src="item.url" class="image" mode="aspectFit" />
						<view class="text">{{ item.title }}</view>
					</view>
				</uni-grid-item>
			</uni-grid>
		</view>
	    <uni-card title="公告" thumbnail="../../static/alarm.png" extra="查看全部">
	        <uni-list v-for="(item ,index) in alarm" :index="index" :key="index">
	            <uni-list-item  :title="item.title"></uni-list-item>
	        </uni-list>
	    </uni-card>
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
						title:"用冷新装",
						url:"../../static/i1.png"
					},
					{
						title:"用冷/热申请",
						url:"../../static/i2.png"
					},
					{
						title:"停冷/热申请",
						url:"../../static/i3.png"
					},
					{
						title:"维修申请",
						url:"../../static/i4.png"
					},{
						title:"缴费变更",
						url:"../../static/i5.png"
					},
					{
						title:"供冷办理流程",
						url:"../../static/i6.png"
					},
					{
						title:"历史数据",
						url:"../../static/i7.png"
					},
					{
						title:"积分商城",
						url:"../../static/i8.png"
					}
				],
				alarm:[
					{
					 title:"1.用冷须知"
					},
					{
					 title:"2.停冷须知"
					}
				]
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
