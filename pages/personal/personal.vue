<template>
	<view class="bigbox">
		<view class="toux">
			<view class="xinxi">
				<image src="../../static/logo.png" mode=""
					style="width: 100rpx;height: 100rpx;border-radius: 100%;margin-right: 10px;"></image>
				<span>海鲜兔子</span>
			</view>
			<van-icon size="35rpx" name="setting" />
		</view>
		<!-- 会员卡 -->
		<view class="card">
			<view class="member">
				<view class="myicon">
					<van-icon name="gem" size="25px" />
					<span>海鲜会员</span>
				</view>
				<span>哪里都是靓丽的风景线</span>
			</view>
			<view class="pay">
				<span>成为会员</span>
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
		padding: 30rpx;

		.toux {
			display: flex;
			justify-content: space-between;
			align-items: center;
			margin-bottom: 30rpx;

			.xinxi {
				display: flex;
				align-items: center;
			}
		}

		.card {
			height: 150rpx;
			width: 100%;
			background: repeating-linear-gradient(to right, #d81406, #dc4035);
			border-radius: 10rpx;
			display: flex;
			justify-content: space-between;
			color: #fff;
			align-items: center;

			.member {
				margin-left: 30rpx;

				span {
					font-size: 12rpx;
				}

				.myicon {
					font-weight: bold;
					display: flex;
					align-items: center;

					span {
						font-size: 24rpx;
					}
				}
			}

			.pay {
				width: 120rpx;
				height: 25%;
				margin-right: 30rpx;
				border: #fff solid;
				border-radius: 25rpx;
				text-align: center;
				display: flex;
				align-items: center;
				justify-content: center;
				font-size: 16rpx;
			}
		}
	}
</style>