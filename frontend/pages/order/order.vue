<!--本页面由uniapp切片工具生成，uni-app切片-可视化设计工具(一套代码编译到7个平台iOS、Android、H5、小程序)，软件下载地址：http://www.ymznkf.com/new_view_669.htm -->
<template>
	<view class="YmContent">
		<view class="all_orders_1">
			<text decode="true" class="all_orders_2">全部订单</text>
			<view class="orders">
				<view v-for="(item_orders, index) in list_orders" :key="index" class="item" >
					<view class="all_orders_5" @tap="gotoOrderDetail(index)">
						<view class="all_orders_7">
							<image src="/static/all_orders/images/all_orders_8_8.jpg" mode="scaleToFill"
							 border="0" class="all_orders_8"></image>
							<text decode="true" class="address_from">{{item_orders.userInfo}}</text>
						</view>
						<image src="/static/all_orders/images/all_orders_10_10.jpg" mode="scaleToFill"
						 border="0" class="all_orders_10"></image>
						<view class="all_orders_11">
							<image src="/static/all_orders/images/all_orders_12_12.jpg"
							 mode="scaleToFill" border="0" class="all_orders_12"></image>
							<text decode="true" class="address_to">{{item_orders.itemInfo}}</text>
						</view>
						<view class="all_orders_14">
							<text decode="true" class="all_orders_15">订单号</text>
							<text decode="true" class="orderNo">{{item_orders.indentNo}}</text>
						</view>
					</view>
					<image :src="geturl(item_orders)" mode="scaleToFill"
					 border="0" class="all_orders_6"></image>
				</view>
			</view>
		</view>
		<br><br><br><br>
	</view>
</template>

<script>
	import all_orders from "./all_orders.js";
	export default all_orders;
</script>

<style lang="scss" scoped>

	@import './all_orders.scss'
</style>


