<template>
	<view class="body">
		<Navigation :home_icon_logo="false"></Navigation>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E6%96%B0%E9%97%BB%E5%92%A8%E8%AF%A2-banner.png" mode="widthFix" style="width: 100%;"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>
		<view class="navigator">
			<navigator class="navigator-item" v-for="(item,index) in news_url" :key="index">
				<image :src="item.icon" mode="" style="height: 41.17rpx;width: 42.35rpx;"></image>
				<text style="padding-left: 23.52rpx;flex: 1;">{{item.title}}</text>
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/ICON.png" mode="" style="height: 35.29rpx; width: 18.82rpx;float: right;"></image>
			</navigator>
			
		</view>
		
		
		<Tarbar></Tarbar>
	</view>
	
</template>

<script>
	import Navigation from "../../components/navigation.vue"
	import Tarbar from '../../components/tarbar.vue'
	
	export default {
		data() {
			return {	
				navigation_is_show:false,
				news_url:[
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon1.png',
						title:'翻译语种',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon2.png',
						title:'口译同传',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon3.png',
						title:'资料笔译',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon4.png',
						title:'本地化翻译',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon5.png',
						title:'翻译领域',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon6.png',
						title:'服务社区',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon7.png',
						title:'特色服务',
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/%E5%92%A8%E8%AF%A2-icon8.png',
						title:'翻译组合',
					}
				]
			}
		},
		components: {
			Navigation,
			Tarbar
			},
		onLoad() {
			this.navigation_is_show=false
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	page{
		// height: 100%;
		flex: 1;
	}
	.body{
			height: 100%;
			font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
			margin-bottom: 50px;
			.banner{
				margin-top: 103.52rpx;
				width: 100%;
				height: 376.47rpx;
				uni-swiper{
					display: block;
					height: 100%;
					
				}
			}
			.menu-bar{
				height: 103.52rpx;
				width: 100%;
				display: block;
				padding: 0 23.52rpx;
				box-sizing: border-box;
				font-size: 37.64rpx;
				line-height: 103.52rpx;
				background-color: hsl(0,0,98%);
				font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
				border-top:1.17rpx hsl(0,0,80%) solid;
				border-bottom:1.17rpx hsl(0,0,80%) 	solid;
				.menu-bar-title{
					border-left-style:solid;
					padding-left: 17.64rpx;
					border-color: hsl(25%,100%,46%);
				}
			}
			
		.navigator{
			width: 100%;
			// height: 100%;
			background-color: hsl(0,0,95%);
			// margin: 10px 0;
			padding-bottom: 5.88rpx;
			.navigator-item{
				margin-bottom: 11.76rpx;
				background-color: #FFFFFF;
				display: flex;
				flex-direction: row;
				align-items: center;
				justify-content: space-between;
				font-size: 32.94rpx;
				width: 100%;
				height: 103.52rpx;
				box-sizing: border-box;
				padding: 35.29rpx 47.05rpx;
			}
		}
		
	}
</style>
