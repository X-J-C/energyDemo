<template>
	<view style="width: 100%;">
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item v-for="(item ,index) in imagelist" :index="index" :key="index">
							<image :src="item.url" class="image" mode="aspectFill" />
						</swiper-item>
						
					</swiper>
				</view>
			</view>
		</view>
		<view style="text-align: center;margin: 10px;">
			<text style="font-size: 36rpx;">欢迎您:{{text}}</text>
		</view>
		<view class="example-body">
			<uni-grid :column="4" :show-border="false" :square="false" >
				<uni-grid-item  v-for="(item ,index) in list" :index="index" :key="index">
					<view class="grid-item-box">
						<view class="title">{{item.title}}</view>
						<view class="num">{{item.num}}</view>
					</view>
				</uni-grid-item>
			</uni-grid>
		</view>
	</view>
	

</template>

<script>
	export default {
		
		data() {
			return {
				imagelist:[
					{
						url:'../../static/banner.jpg'
					},
					{
						url:'../../static/banner1.jpg'
					},
					{
						url:'../../static/banner2.png'
					}
				],
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
				text:"丽新文创",
				list: [
					{
						title:"本月冷量",
						num:0
					},
					{
						title:"本月冷费",
						num:0
					},
					{
						title:"本月热量",
						num:0
					},
					{
						title:"本月热费",
						num:0
					},
				]
				
			}
		},
		methods: {

		}
	}
</script>

<style>
	.uni-margin-wrap {
		width: 690rpx;
		margin: 0 30rpx;
	}

	.swiper {
		height: 300rpx;
	}

	.swiper-item {
		display: block;
		height: 300rpx;
		line-height: 300rpx;
		text-align: center;
	}

	.swiper-list {
		margin-top: 40rpx;
		margin-bottom: 0;
	}

	.uni-common-mt {
		margin-top: 60rpx;
		position: relative;
	}

	.info {
		position: absolute;
		right: 20rpx;
	}

	.uni-padding-wrap {
		width: 100%;
		padding: 10rpx 0;
	}
	
    .example-body{
	    text-align: center;
		background-color: #fff;
		border-radius: 5px;
	}
	.num{
	  font-weight: bold;
	  font-size: 36rpx;
	}
   .image{
	  height: 100%;
	  width: 100%;
	}
	
	
	
	
</style>
