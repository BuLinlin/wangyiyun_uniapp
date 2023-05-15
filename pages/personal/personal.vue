<template>
	<view class="bigbox">
		<!-- 登录后的效果 -->
		<view class="onebox" v-if="userInfo.nickName">
			<!-- 头像 -->
			<image :src="userInfo.avatarUrl" mode=""
				style="position:absolute;top:-25%;width:100rpx;height: 100rpx; border-radius: 50%;"></image>
			<!-- 用户名与vip -->
			<view class="information">
				<span class="sp1" style="font-size: 33rpx;font-weight: bold;">{{userInfo.nickName}}</span>
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
		<!-- 登录前的效果 -->
		<view class="twobox" v-else>
			<!-- 头像 -->
			<image src="@/static/logo.png" mode=""
				style="position:absolute;top:-25%;width:100rpx;height: 100rpx; border-radius: 50%;"></image>
			<!-- 立即登录 -->
			<view class="information">
				<button open-type="getUserInfo" @tap="getUserinfo" @click="getlogin()" class="sp1"
					style="font-size: 40rpx;font-weight: bold;">立即登录></button>
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
				userInfo: {}
			};
		},
		created() {
			wx.getStorage({
				key: "userInfo",
				success: (res) => {
					if (res.data) {
						this.userInfo = JSON.parse(res.data)
					}
				}
			})
		},
		methods: {
			async getlogin(){
				const login = await this.$myRequest({
					url:"/register/anonimous"
				})
				wx.setStorageSync('cookie', login.data.cookie);
				console.log(login.data.cookie)
			},
			getUserinfo(data) {
				// 推荐使用wx.getUserProfile获取用户信息，开发者每次通过该接口获取用户个人信息均需用户确认
				// 开发者妥善保管用户快速填写的头像昵称，避免重复弹窗
				wx.getUserProfile({
						desc: '用于完善会员资料', // 声明获取用户个人信息后的用途，后续会展示在弹窗中，请谨慎填写
						success: (res) => {
							// 保存用户信息
							wx.setStorage({
								key: "userInfo",
								data: JSON.stringify(res.userInfo)
							})
							uni.showToast({
								title: '登录成功！，即将回到首页'
							})
							// 跳转页面
							uni.reLaunch({
								url:'/pages/index/index'
							})
						}
					})
			}
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

			.grade {
				font-size: 22rpx;
				display: flex;
				color: #868686;
				margin-top: 2%;
				width: 33%;
				justify-content: space-around;
				align-items: center;
				margin-bottom: 5%;

				.segmentation {
					width: 3rpx;
					height: 20rpx;
					background-color: #868686;
				}
			}
		}

		.twobox {
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
			min-height: 180rpx;
		}
	}
</style>