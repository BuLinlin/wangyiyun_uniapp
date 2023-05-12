<template>
	<view class="bigbox">
		<view class="onebox">
			<!-- 头像 -->
			<image src="@/static/logo.png" mode=""
				style="position:absolute;top:-25%;width:100rpx;height: 100rpx; border-radius: 50%;"></image>
			<!-- 用户名与vip -->
			<view class="information">
				<span class="sp1" style="font-size: 33rpx;font-weight: bold;">海鲜兔子</span>
				<view class="nameplate">
					<van-tag type="danger" round>svip</van-tag>
				</view>
			</view>
			<!-- 关注人数/粉丝数/用户等级 -->
			<view class="grade">
				<span>6关注</span>
				<!-- 分割线 -->
				<view class="segmentation"> </view>
				<span>1粉丝</span>
				<!-- 分割线 -->
				<view class="segmentation"> </view>
				<span>LV.6</span>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		components: {

		},
		data() {
			return {

			};
		}
	}
</script>

<style lang="less" scoped>
	.bigbox {
		padding: 5%;
		background-color: rgb(245, 245, 245);
		min-height: 100vh;
		.onebox {
			margin-top: 10%;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			background-color: #fff;
			height: auto;
			border-radius: 20rpx;
			box-shadow: 0 0 200rpx 2rpx rgba(0, 0, 0, 0.1);
			position: relative;

			.information {
				margin-top: 10%;
				display: flex;
				width: 33%;
				justify-content: space-around;
				align-items: center;

				.sp1 {
					white-space: nowrap;
				}

				.nameplate {
					font-size: 14rpx;
				}
			}
			.grade{
				font-size: 22rpx;
				display: flex;
				color: #868686;
				margin-top: 2%;
				width: 33%;
				justify-content: space-around;
				align-items: center;
				margin-bottom: 5%;
				.segmentation{
					width: 3rpx;
					height: 20rpx;
					background-color: #868686;
				}
			}
		}
	}
</style>