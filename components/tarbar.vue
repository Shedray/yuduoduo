<template>
	<view class="tarbar">
		<uni-grid :column="4" :square="false" :showBorder="false">
		    <uni-grid-item>
				<navigator :class="{'uni-grid-item':true,'selected':selected==1}" url="/pages/index/index"> 
				<image v-if="selected==1" src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-1-se.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
				<image v-else src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-1-no.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
									<text>首页</text>
				</navigator>
		    </uni-grid-item>
		   <uni-grid-item>
		      <navigator :class="{'uni-grid-item':true,'selected':selected==2}" >
				<image v-if="selected==2" src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-2-se.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
				<image v-else src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-2-no.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
						      	<text>在线咨询</text>
		      </navigator>
		   </uni-grid-item>
		   <uni-grid-item>
			  <navigator :class="{'uni-grid-item':true,'selected':selected==3}" url="/pages/services/services">
				<image v-if="selected==3" src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-3-se.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
				<image v-else src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-3-no.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
				
				<text>申请服务</text>
			  </navigator>
		   </uni-grid-item>
		   <uni-grid-item>
		     <navigator :class="{'uni-grid-item':true,'selected':selected==4}" >
				<image v-if="selected==4" src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-4-se.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
				<image v-else src="https://qcloudtest-1252037166.cos.ap-guangzhou.myqcloud.com/yuduoduo/index_asset/home-table-4-no.png" mode="" style="height: 54.11rpx;width: 54.11rpx"></image>
						     	<text>电话咨询</text>
		     </navigator>
		   </uni-grid-item>
		</uni-grid>
		
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
	export default {
		name:'Tarbar',
		props:{
			selected: {
				type: Number,
				default: 1
			}
		},
		data() {
			return {
				
			};
		},
		components:{
			uniGrid,
			uniGridItem
		}
	}
</script>

<style lang="scss">
	.tarbar{
		// font-family:"Microsoft YaHei",微软雅黑,"Microsoft JhengHei",华文细黑,STHeiti,MingLiu;
		width: 100%;
		height: 50px;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		position: fixed;
		z-index: 1;
		bottom: 0;
		left: 0;
		border-top:1.17rpx hsl(0,0,80%) solid;
		color: rgb(192, 196, 204);
		background-color: #FFFFFF;
			.uni-grid-item{
				display: flex;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				flex: 1;
				height: 50px;
				font-size: 10px;
				
				text{
					margin-top: 4px;
				}
			}
			.selected{
				color: rgb(255, 152, 0);
			}
		
		
	}
</style>
