<template>
	<view class="bigbox">
		<view class="onebox">
			<span style="font-size: 33rpx;font-weight: bold;">推荐电台<van-icon name="arrow" /></span>
		</view>
		<view class="twobox">
			<view class="litbox" v-for="item in radio" :key="item.id">
				<image :src="item.picUrl" mode="" style="width: 600rpx;height: 300rpx;border-radius: 20rpx;"></image>
				<van-icon class="ico" name="live" size="50" color="#fff" />
				<view class="card">
					<span>{{item.rcmdtext}}</span>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				radio: [{
						id: 975555134,
						name: "亲历者说",
						picUrl: "https://p2.music.126.net/l-cV-8MkI1UCaliceQAAbg==/109951167742698767.jpg",
						programCount: 60,
						subCount: 15303,
						createTime: 1650770940651,
						categoryId: 3080097,
						category: "故事",
						rcmdtext: "聚焦热点事件，连线亲历者，亲自讲述人情冷暖。",
						radioFeeType: 0,
						feeScope: 0,
						playCount: 20609732,
						subed: false,
						dj: {
							defaultAvatar: false,
							province: 110000,
							authStatus: 0,
							followed: false,
							avatarUrl: "http://p1.music.126.net/sOVROsQ-5OCW-xEl58s6fA==/109951167152437495.jpg",
							accountStatus: 0,
							gender: 2,
							city: 110101,
							birthday: -2209017600000,
							userId: 4942507138,
							userType: 205,
							nickname: "人间剧场",
							signature: "烟火人间里的百味人生",
							description: "",
							detailDescription: "",
							avatarImgId: 109951167152437490,
							backgroundImgId: 109951162868128400,
							backgroundUrl: "http://p1.music.126.net/2zSNIqTcpHL2jIvU6hG0EA==/109951162868128395.jpg",
							authority: 0,
							mutual: false,
							expertTags: null,
							experts: null,
							djStatus: 10,
							vipType: 0,
							remarkName: null,
							authenticationTypes: 16384,
							avatarDetail: null,
							avatarImgIdStr: "109951167152437495",
							backgroundImgIdStr: "109951162868128395",
							anchor: false,
							avatarImgId_str: "109951167152437495"
						},
						copywriter: "由亲历者自己讲述的热点故事",
						buyed: false
					},
					{
						id: 965024140,
						name: "他和她的那些故事",
						picUrl: "https://p2.music.126.net/7msFCPWwG3lQ_N_WwOMy-A==/109951166279108083.jpg",
						programCount: 8,
						subCount: 518,
						createTime: 1628003549039,
						categoryId: 3,
						category: "情感",
						rcmdtext: null,
						radioFeeType: 0,
						feeScope: 0,
						playCount: 276297,
						subed: false,
						dj: {
							defaultAvatar: false,
							province: 110000,
							authStatus: 0,
							followed: false,
							avatarUrl: "http://p1.music.126.net/sadA8PjvJ1DZpxB8J42JSA==/109951164412306524.jpg",
							accountStatus: 0,
							gender: 1,
							city: 110101,
							birthday: 680972400000,
							userId: 98245332,
							userType: 205,
							nickname: "十三和八一",
							signature: "三十岁，是重新开始的人生。",
							description: "",
							detailDescription: "",
							avatarImgId: 109951164412306530,
							backgroundImgId: 109951162868126480,
							backgroundUrl: "http://p1.music.126.net/_f8R60U9mZ42sSNvdPn2sQ==/109951162868126486.jpg",
							authority: 0,
							mutual: false,
							expertTags: null,
							experts: null,
							djStatus: 10,
							vipType: 11,
							remarkName: null,
							authenticationTypes: 16384,
							avatarDetail: null,
							avatarImgIdStr: "109951164412306524",
							backgroundImgIdStr: "109951162868126486",
							anchor: false,
							avatarImgId_str: "109951164412306524"
						},
						copywriter: "【独家】知名媒体从业人员 温暖情感声优",
						buyed: false
					},
					{
						id: 963307048,
						name: "新闻早餐",
						picUrl: "https://p2.music.126.net/XwB_01uMMXd5py_XetTrIw==/109951166132208015.jpg",
						programCount: 631,
						subCount: 65085,
						createTime: 1624349374640,
						categoryId: 3087096,
						category: "新闻资讯",
						rcmdtext: "3分钟速听今日大事",
						radioFeeType: 0,
						feeScope: 0,
						playCount: 77795461,
						subed: false,
						dj: {
							defaultAvatar: false,
							province: 110000,
							authStatus: 1,
							followed: false,
							avatarUrl: "http://p1.music.126.net/SUeqMM8HOIpHv9Nhl9qt9w==/109951165647004069.jpg",
							accountStatus: 0,
							gender: 0,
							city: 110101,
							birthday: -2209017600000,
							userId: 5052347559,
							userType: 10,
							nickname: "中国新闻网",
							signature: "",
							description: "中国新闻网官方账号",
							detailDescription: "中国新闻网官方账号",
							avatarImgId: 109951165647004060,
							backgroundImgId: 109951162868126480,
							backgroundUrl: "http://p1.music.126.net/_f8R60U9mZ42sSNvdPn2sQ==/109951162868126486.jpg",
							authority: 0,
							mutual: false,
							expertTags: null,
							experts: null,
							djStatus: 10,
							vipType: 0,
							remarkName: null,
							authenticationTypes: 18432,
							avatarDetail: null,
							avatarImgIdStr: "109951165647004069",
							backgroundImgIdStr: "109951162868126486",
							anchor: false,
							avatarImgId_str: "109951165647004069"
						},
						copywriter: "今天发生了大事？3分钟速听！",
						buyed: false
					},
				]
			}
		},
		mounted() {
			this.getradiolist()
		},
		methods: {
			async getradiolist() {
				const res = await this.$myRequest({
					url: "/dj/recommend"
				})
				this.radio = res.data.djRadios
				console.log(this.radio)
			}
		}
	}
</script>

<style lang="less" scoped>
	.bigbox {
		padding: 5%;
		display: flex;
		flex-direction: column;

		.onebox {
			margin-bottom: 30rpx;
		}

		.twobox {
			display: flex;
			overflow: auto;

			.litbox {
				position: relative;
				margin-left: 2%;

				.ico {
					position: absolute;
					left: 50%;
					top: 50%;
					transform: translate(-50%, -50%);
				}

				.card {
					box-sizing: border-box;
					width: 600rpx;
					overflow: hidden;
					padding: 2%;
					position: absolute;
					bottom: 0;
					color: #fff;
					border-bottom-left-radius: 20rpx;
					border-bottom-right-radius: 20rpx;
					white-space: nowrap;
					text-overflow: ellipsis;
					background-color: rgba(0, 0, 0, 0.5);
				}
			}
		}
	}
</style>