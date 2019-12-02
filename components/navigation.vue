<template>
	<view class="header">
		<view class="header-icon" v-if="home_icon_logo">
			<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/logo.png" mode="widthFix" style="height: 68.23rpx; width: 172.94rpx;"></image>
		</view>
		<view class="" v-else style="padding: 23.52rpx;">
			<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/news_assets/ICON.png" mode="" style="height: 47.05rpx;width: 35.29rpx;transform:rotate(180deg)"></image>
		</view>
		<view class="" v-if="home-title">
			<text>删除</text>
		</view>
		<view class="header-icon" style="padding: 23.52rpx;" @tap="navigation_show">
			<image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-icon.png" mode="widthFix" style="width: 38.82rpx;height: 23.52rpx;"></image>	
		</view>
		<view class="navigation" v-if="navigation_is_show">
				<navigator url="/pages/index/index">
					<text>首页</text>
				</navigator>
				<navigator url="/pages/tran_bypen/tran_bypen">
					<text>笔译翻译</text>
				</navigator>
				<navigator url="/pages/trans/trans">
					<text>口译翻译</text>
				</navigator>
				<navigator url="/pages/index_local/index_local">
					<text>本地化翻译</text>
				</navigator>
				<navigator url="/pages/news/news">
					<text>新闻咨询</text>
				</navigator>
				<navigator url="" style="border-bottom:none">
					<text>注册</text>
				</navigator>
			</view>
		</view>
	</view>
	
</template>

<script>
	export default {
		name:'Navigation',
		props:{
			home_icon_logo:{
				type:Boolean,
				default:true
			},
		
			home_title:{
				type:Boolean,
				default:false
			}
		},
		data() {
			return {
				navigation_is_show:false
			};
		},
		methods:{
			navigation_show:function(){
				this.navigation_is_show=~this.navigation_is_show
			}
		}
	}
</script>

<style lang="scss">
	.header{
		font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
		
		top: 0;
		height: 103.52rpx;
		width: 100%;
		display: flex;
		flex-direction:row ;
		align-items: center;
		justify-content: space-between;
		box-sizing: border-box;
		padding: 0 23.52rpx;
		position: fixed;
		z-index: 1;
		background-color: #FFFFFF;
		.header-icon{
			
			display: flex;
			flex-direction: row;
			align-items: center;
		}
		.navigation{
						top: 103.52rpx;
						right: 23.52rpx;
						z-index: 1;
						position: fixed;
						background-image: url(https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/navigation_bg.png);
						background-size: 100% 100%;
						// height: 376.47rpx;
						width: 211.76rpx;
						padding: 23.52rpx 0;
						box-sizing: border-box;
						navigator{
							font-size: 25.88rpx;
							color: #FFFFFF;
							display: flex;
							flex-direction: row;
							justify-content: center;
							box-sizing: border-box;
							margin: 0 23.52rpx;
							padding: 16.47rpx 0;
							border-bottom:1.17rpx #888 	solid;
						}
					}
	}
	
</style>
