<template>
	<view class="body">
		<Navigavition></Navigavition>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-banner.png" mode="widthFix" style="width: 100%;"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>
		<Tarbar></Tarbar>
		
		<view class="service">
			<view class="menu-bar">
						<text class="menu-bar-title">本地化服务分类</text>
			</view>
			<view class="service-type"  v-for="(item,index) in service_type" :key="index">
				<view class="service-type-icon">
					<image :src="item.icon" mode="" style="height: 129.41rpx;width: 129.41rpx;"></image>
				</view>
				<view class="service-type-text">
					<text class="service-type-text-title">
						{{item.title}}
					</text>
					<text class="service-type-text-context">
						{{item.context}}
					</text>
				</view>
			</view>
			
		</view>
		<view class="service-strengths">
			<view class="menu-bar">
						<text class="menu-bar-title">本地化服务优势</text>
			</view>
			<view class="service-strengths-content">
				<uni-grid :column="2" :square="false" :showBorder="false">
				    <uni-grid-item v-for="(item,index) in service_strengths" :key="index">
				        <view class="service-strengths-item">
				        	<image :src="item.icon" mode="" style="height: 100%;width: 100%;"></image>
						</view>
				    </uni-grid-item>
				   
				</uni-grid>
			</view>
			
		</view>
		<view class="after-sale">
			<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-%E5%94%AE%E5%90%8E%E6%89%BF%E8%AF%BA.png" mode="" style="width: 100%;height: 364.7rpx;margin-top: 11.76rpx;"></image>
		</view>
		
	
		
		
		<view class="login">
			<view class="login-button">
				<text>立即注册</text>
			</view>
		</view>
		
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
	import Navigavition from "../../components/navigation.vue"
	import Tarbar from '../../components/tarbar.vue'
	export default {
		data() {
			return {
				service_type:[
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96_image_1-1.png',
						title:'软件本地化',
						context:'软件源代码资源文件本地化、软件用户界面本地化、联机帮助系统本地化、文档、手册本地化等。'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96_image_1-2.png',
						title:'网站本地化',
						context:'语多多与多家全球知名网站保持长期合作关系，为这些网站提供中文本地化服务。拥有丰厚的经验，专业的翻译流程。'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96_image_1-3.png',
						title:'多媒体本地化',
						context:'语言听译、多语言视频字幕制作、多语言配音、多语言脚本翻译。'
					}
				],
				service_strengths:[
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image1.png'
					},
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image2.png'
					},
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image3.png'
					},
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image4.png'
					},
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image5.png'
					},
					{
						'icon':'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/local_assets/%E6%9C%AC%E5%9C%B0%E5%8C%96-image6.png'
					}
				],
			}
		},
		components: {
			uniGrid,
			uniGridItem,
			Navigavition,
			Tarbar
			},
		onLoad() {

		},
		methods: {
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
			.service{
				margin-bottom: 23.52rpx;
				.service-type{
					padding: 0 23.52rpx;
					padding-top: 23.52rpx;
					height: 184.7rpx;
					box-sizing: border-box;
					border-bottom:1.17rpx hsl(0,0,80%) solid;
					width: 100%;
					display: flex;
					flex-direction:row ;
					.service-type-text{
						display: flex;
						flex-direction: column;
						padding-left: 23.52rpx;
						font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
						.service-type-text-title{
							font-size: 32.94rpx;
							padding: 11.76rpx 0;
						}
						.service-type-text-context{
							font-size: 21.17rpx;
						}
					}
					
				}
			}
			.service-strengths{
				.service-strengths-content{
					padding: 11.76rpx;
					box-sizing: border-box;
					.service-strengths-item{
						height: 235.29rpx;
						width: 100%;
						padding: 11.76rpx;
						
						box-sizing: border-box;
					}
				}
			}
		.login{
			background-color: hsl(0%,0%,98%);
			width: 100%;
			height: 164.7rpx;
			display: flex;
			justify-content: center;
			align-items: center;
			margin-bottom: 50px;
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
