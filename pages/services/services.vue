<template>
	<view class="body">
		<Navigation></Navigation>
		<view class="banner">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
			                        <swiper-item>
			                            <image src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/service_assets/%E6%B3%A8%E5%86%8C-image.png" mode="widthFix" style="width: 100%;"></image>
			                        </swiper-item>
			                        
			                    </swiper>
		</view>
		<view class="form">
			<view class="form-title">
				——  快速获取报价单  ——
			</view>
			<view class="form-item">
			
				<text style="padding:0 23.52rpx; font-size: 32.94rpx;">公司名称:</text>
				<input class="form-item-input" focus placeholder="请填写公司全称"  v-model="data.company"/>
			</view>
			<view class="form-item">
			
				<text style="padding:0 23.52rpx; font-size: 32.94rpx">联系姓名:</text>
				<input class="form-item-input" focus placeholder="请填写本人姓名" v-model="data.name"/>
			</view>
			<view class="form-item">
			
				<text style="padding:0 23.52rpx; font-size: 32.94rpx;">联系电话:</text>
				<input class="form-item-input" focus placeholder="请填写本人手机号" v-model="data.phone"/>
			</view>
			<view class="form-item">
			
				<text style="padding:0 23.52rpx; font-size: 32.94rpx;">翻译语种:</text>
				<input class="form-item-input" focus placeholder="选择翻译语种"  v-model="data.lang"/>
			</view>
			<view class="form-item">
			
				<text style="padding:0 23.52rpx; font-size: 32.94rpx;">需求类型:</text>
				<input class="form-item-input" focus placeholder="选择需求类型"  v-model="data.needs"/>
			</view>
			<view class="button" @tap="commit">
				立即提交
			</view>
		</view>
		
		
		<Tarbar :selected="3"></Tarbar>
	</view>
	
</template>

<script>
	import Navigation from "../../components/navigation.vue"
	import Tarbar from '../../components/tarbar.vue'
	
	export default {
		data() {
			return {	
				navigation_is_show:false,
				data:{
					company:'',
					phone:'',
					name:'',
					lang:'',
					needs:''
				}
				
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
			commit:function(){
				console.log(this.data)
			},
		}
	}
</script>

<style lang="scss">
	.body{
		background-color: #007AFF;
		
			height: 100%;
			font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
			.banner{
				margin-top: 103.52rpx;
				width: 100%;
				height: 376.47rpx;
				background-color: hsl(0,0,96%);
				uni-swiper{
					display: block;
					height: 100%;
					
				}
			}
			.menu-bar{
				height: 50px;
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
			
		
		.form{
			padding: 30rpx 0;
			flex: 1;
			width: 100%;
			height: 100%;
			display: flex;
			flex-direction: column;
			background-color: hsl(0,0,96%);
			align-items: center;
			.form-title{
				font-size: 44.7rpx;
				color: hsl(25%,100%,50%);
				margin-bottom: 50rpx;
			}
			.form-item{
				
				display: flex;
				flex-direction: row;
				align-items: center;
				padding: 11.76rpx 0;
				font-size: 140px;
				.form-item-input{
					border:1.17rpx hsl(0,0,80%) solid;
					border-radius: 4px;
					height: 58.82rpx;
					width: 352.94rpx;
					font-size: 28.23rpx;
					background-color: #FFFFFF;
					padding: 4.7rpx 23.52rpx;
				}
			}
			.button{
				margin-top: 58.82rpx;
				height: 84.7rpx;
				width: 376.47rpx;
				display: flex;
				justify-content: center;
				align-items: center;
				background-color: hsl(25%,100%,46%);
				color: #FFFFFF;
				border-radius: 11.76rpx;
				font-size: 35.29rpx;
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
