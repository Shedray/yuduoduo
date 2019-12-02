<template>
	<view class="body">
		<Navigation></Navigation>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/trans_assets/%E5%8F%A3%E8%AF%91-banner.png" mode="widthFix" style="width: 100%;"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>

		
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">口译项目介绍</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/trans_assets/trans_image1.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">口译翻译类型</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/trans_assets/trans_image2.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">口译服务流程</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/trans_assets/trans_image3.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">口译服务语种</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/trans_assets/trans_image4.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="login">
			<view class="login-button">
				<text>立即注册</text>
			</view>
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
				navigation_is_show:false
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
			select_news_type:function(value){
				this.news_type=value
			},
		}
	}
</script>

<style lang="scss">
	.body{
			
			font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
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
			
		
		.lang-service{
			.lang-service-type{
				padding: 35.29rpx 35.29rpx;
			}
		
		}
		.login{
			margin-top: -11.76rpx;
			width: 100%;
			height: 164.7rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			margin-bottom: 50px;
			background-color: hsl(0%,0%,98%);
			.login-button{
				height: 84.7rpx;
				width: 407.05rpx;
				display: flex;
				justify-content: center;
				align-items: center;
				background-color: hsl(25%,100%,46%);
				color: #FFFFFF;
				border-radius: 84.7rpx;
				font-size: 35.29rpx;
			}
		}
		
	}
</style>
