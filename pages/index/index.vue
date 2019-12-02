<template>
	<view class="body">
		<Navigation></Navigation>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/%E9%A6%96%E9%A1%B5-banner2.png" mode="" style="width: 100%;height: 100%"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>
		<view class="service">
			<view class="menu-bar">
						<text class="menu-bar-title">服务分类</text>
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
		
		
		<view class="trans-service">
			<view class="menu-bar">
						<text class="menu-bar-title">翻译服务流程</text>
			</view>
			<view class="trans-service-content">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/trans-service.png" mode="widthFix" style="width: 100%"></image>
			</view>
			
		</view>
		<view class="lang-service">
			<view class="menu-bar">
						<text class="menu-bar-title">语言服务</text>
			</view>
			<view class="lang-service-type">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/lang-service.png" mode="widthFix" style="width: 100%;"></image>
			</view>
		</view>
		<view class="solu-plan">
			<view class="menu-bar">
						<text class="menu-bar-title">解决方案</text>
			</view>
			<view class="solu-plan-content">
				<uni-grid :column="2" :square="false" :showBorder="false">
				    <uni-grid-item v-for="(item,index) in solu_plan" :key="index">
				        <view class="solu-plan-content-item">
				        	<image :src="item.icon" mode="" style="height: 134.11rpx;width: 134.11rpx;"></image>
							<text class="solu-plan-content-item-title">{{item.title}}</text>
							<view style="border-top:1.17rpx hsl(0,0,80%) solid;display: block;height: 11.76rpx;width: 11.76rpx;">
									
							</view>
							<view class="solu-plan-content-item-content">
								<text v-for="(text,index) in item.context" :key="index">
									{{text}}
								</text>
								
							</view>
						</view>
				    </uni-grid-item>
				   
				</uni-grid>
			</view>
			
		</view>
		<view class="">
			<view class="menu-bar">
						<text class="menu-bar-title">服务优势</text>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/index_%E6%9C%8D%E5%8A%A1%E4%BC%98%E5%8A%BF1.png" mode="widthFix" style="width: 100%;"></image>
				
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-image1.png" mode="widthFix" style="width: 100%;"></image>
			</view>
			<view class="" style="">
				<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/index_%E6%9C%8D%E5%8A%A1%E4%BC%98%E5%8A%BF2.png" mode="widthFix" style="width: 100%;"></image>
			</view>
		</view>
		<view class="news">
			<view class="menu-bar">
						<text class="menu-bar-title">新闻资讯</text>
			</view>
			<view class="news-tab">
				<!-- <view class="news-tab"> -->
					<view :class="{'news-tab-item':true,'news-tab-item-selected':news_type==1}" @tap="select_news_type(1)">
							<text>同声传译</text>
					</view>
					<view :class="{'news-tab-item':true,'news-tab-item-selected':news_type==2}"  @tap="select_news_type(2)">
							<text>资料笔译</text>
					</view>
					<view :class="{'news-tab-item':true,'news-tab-item-selected':news_type==3}"  @tap="select_news_type(3)">
							<text>本地化翻译</text>
					</view>
					<view :class="{'news-tab-item':true,'news-tab-item-selected':news_type==4}"  @tap="select_news_type(4)" style="border: none;">
							<text>翻译案例</text>
					</view>
			</view>
			<view class="news-content">
				<navigator class="news-content-item" v-for="(item,index) in news_data" :key="index">
					<text>{{item.title}}</text>
					<text style="padding-left: 35.29rpx;">{{item.data}}</text>
				</navigator>
				
			</view>
			<view class="news-more">
				<text>查看更多>></text>
				
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
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home_image_1-1.png',
						title:'笔译翻译',
						context:'商务文件、公司文件、法律文件、专业资料、技术手册、专利翻译、公证材料、医疗材料等'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home_image_1-2.png',
						title:'口译翻译',
						context:'同声传译、交替传译、商务口译、陪同口译、旅游口译、会议口译、技术口译、谈判口译、法庭口译、双语主持、医疗口译、现场派驻'
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home_image_1-3.png',
						title:'本地化翻译',
						context:'软件本地化、网络本地化、文档本地化、多媒体本地化等'
					}
				],
				solu_plan:[
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88-icon1.png',
						title:'法律财经',
						context:[
							'律师级翻译专家',
							'法学界译审团队',
							'高品质翻译服务',
							'严格的保密机制']
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88-icon2.png',
						title:'游戏动漫',
						context:[
							'千万字游戏动漫翻译经验',
							'提前全面了解游戏内容',
							'目标市场定制化语言风格',
							'专业化CAT本地化软件']
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88-icon3.png',
						title:'建筑工程',
						context:[
							'工程项目标书翻译',
							'建筑工程图纸翻译',
							'施工技术说明翻译',
							'母语工程翻译专家']
					},
					{
						icon:'https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88-icon4.png',
						title:'生物医药',
						context:[
							'5000名专业语言学家',
							'IS09001质量管理认证',
							'一译、二改、三校、四审',
							'行业领先的国际专家']
					}
				],
				news_type:1,
				news_data:[{
					title:'如何做好法律翻译（一）：提高思维能力',
					data:'04-24'
				},
				{
					title:'如何做好法律翻译（一）：提高思维能力',
					data:'04-24'
				},
				{
					title:'如何做好法律翻译（一）：提高思维能力',
					data:'04-24'
				},
				{
					title:'如何做好法律翻译（一）：提高思维能力',
					data:'04-24'
				},
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
		.trans-service{
			.trans-service-content{
				padding: 20px;
				box-sizing: border-box;
			}
		}
		.lang-service{
			.lang-service-type{
				padding: 35.29rpx 35.29rpx;
			}
		}
		.solu-plan{
			.solu-plan-content{
				.solu-plan-content-item{
					height: 456.47rpx;
					width: 336.47rpx;
					margin: 23.52rpx;
					border:1.17rpx hsl(0,0,80%) solid;
					padding: 23.52rpx;
					box-sizing: border-box;
					display: flex;
					flex-direction: column;
					align-items: center;
					font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
					.solu-plan-content-item-title{
						margin-top: 47.05rpx;
						font-size: 35.29rpx;
					}
					.solu-plan-content-item-content{
						margin-top: 11.76rpx;
						height: 129.41rpx;
						display: flex;
						flex-direction: column;
						align-items: center;
						font-size: 23.52rpx;
						text{
							padding: 3px;
						}
					}
				}
			}
		}
		.news{
			.news-tab{
				height: 94.11rpx;
				width: 100%;
				font-size: 32.94rpx;
				font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
				display: flex;
				flex-direction: row;
				justify-content: center;
				align-items: center;
				box-sizing: border-box;
				border-bottom:1.17rpx hsl(0,0,80%) 	solid;
				
				.news-tab-item{
					padding: 0 23.52rpx;
					border-right:1.17rpx hsl(0,0,80%) solid;
					height: 100%;
					display: flex;
					flex-direction: row;
					align-items: center;
					justify-content: center;
					
					&:nth-last-child{
						
					}
				}
				.news-tab-item-selected{
					background-color: hsl(25%,100%,46%);
					color: #FFFFFF;
					border-right:none;
				}
				
			}
			.news-content{
				margin-top: 4.7rpx;
				width: 100%;
				display: block;
				padding: 23.52rpx;
				font-size: 30.58rpx;
				box-sizing: border-box;
				.news-content-item{
					box-sizing: border-box;
					padding:  16.47rpx;
					display: flex;
					flex-direction: row;
					justify-content: space-between;
					
				}
			}
			.news-more{
				height: 77.64rpx;
				width: 100%;
				display: flex;
				flex-direction: row;
				justify-content: center;
				font-size: 23.52rpx;
				align-items: center;
				color: hsl(0,0,40%);
				border-top:1.17rpx hsl(0,0,80%) 	solid;
				border-bottom:1.17rpx hsl(0,0,80%) 	solid;
				
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
