<template>
	<view class="body">
		<Navigation></Navigation>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/%E9%A6%96%E9%A1%B5-banner2.png" mode="widthFix" style="width: 100%;"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>
		<view class="service">
			<view class="menu-bar">
						<text class="menu-bar-title">笔译项目</text>
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
		
		
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">翻译标准</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/trans_bypen_image1.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">翻译标准</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/trans_bypen_image2.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">翻译标准</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/trans_bypen_image3.png" mode="widthFix" style="width: 100%;"></image>
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
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
	import Navigation from "../../components/navigation.vue"
	import Tarbar from '../../components/tarbar.vue'
	
	export default {
		data() {
			return {
				service_type:[
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/%E9%A1%B9%E7%9B%AE_image_1-1.png',
						title:'技术手册',
						context:'专利说明书、产品说明书、行业标准、技术标准、设计规范、可行性研究报告、安装手册、维修手册、零部件手册、工艺流程等。'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/%E9%A1%B9%E7%9B%AE_image_1-2.png',
						title:'法律文件',
						context:'法律文书、法律合同、法律专利、法律技术规范、律师函、法律判决书、行业管理规定、公司管理规定、法律法规、公告通知、委托书等。'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/%E9%A1%B9%E7%9B%AE_image_1-3.png',
						title:'经济贸易',
						context:'公司简介、公司章程、合同协议、产品目录、企划书、销售手册、宣传手册、市场调研、财务报告、审计报告、商业信函、传真、备忘录等。'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/tran_bypen_assets/%E9%A1%B9%E7%9B%AE_image_1-4.png',
						title:'公证材料',
						context:'出生证、结婚证、离婚证、户口本、个人简历、入学申请、学历证书、成绩单、求职申请、签证申请、证明材料、往来信件、邀请信、委托书等。'
					}
				],
				
				
				navigation_is_show:false
			}
		},
		components: {
			uniGrid,
			uniGridItem,
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
