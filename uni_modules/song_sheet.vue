<template>
	<view class="bigbox">
		<view class="onebox">
			<span style="font-size: 33rpx;font-weight: bold;">推荐歌单<van-icon name="arrow" /></span>
		</view>
		<view class="card">
			<view class="recommend">
				<view class="one">
					<swiper :indicator-dots="false" :autoplay="true" :interval="3000" :duration="1000" vertical="true"
						circular="true" style="height: 350rpx;">
						<swiper-item v-for="item in imgs" :key="item.id" @touchmove.stop="">
							<view class="swiper-item">
								<image :src="item.picUrl" mode="scaleToFill"
									style="width: 240rpx; height: 240rpx;border-radius: 20rpx;vertical-align:middle;margin-bottom: 10rpx;">
								</image>
								<van-icon class="ico" color="#fff" name="fire" />
								<span class="van-multi-ellipsis--l2">{{item.name}}</span>
							</view>
						</swiper-item>
					</swiper>
				</view>
				<view class="two">
					<view class="recommend2" v-for="item2 in imgs2" :key="item2.id">
						<image :src="item2.picUrl" mode="scaleToFill"
							style="width: 240rpx; height: 240rpx;border-radius: 20rpx;vertical-align:middle;margin-bottom: 10rpx;">
						</image>
						<view class="ico">
							<van-icon color="#fff" name="play" />
							<span style="color: #fff;font-size: 24rpx;:font-weight: bold;">{{formatNum(item2.playCount)}}</span>
						</view>
						<span class="van-multi-ellipsis--l2">{{item2.name}}</span>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgs: [{
						id: 2983726621,
						type: 0,
						name: "成长篇 | 认识到自己的平凡，并且接受",
						copywriter: "",
						picUrl: "https://p1.music.126.net/em_fXgUJDApoV_3_8HYkNg==/109951164362973668.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1681971013514,
						playCount: 30213084,
						trackCount: 100,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 171037362,
						type: 0,
						name: "香港电影中的50首经典歌曲 [追忆录]",
						copywriter: "",
						picUrl: "https://p1.music.126.net/aRMEx-fiTudOmPIhkOe41g==/109951165493447833.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1683686598757,
						playCount: 42031980,
						trackCount: 52,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 652762973,
						type: 0,
						name: "时间治愈的是 愿意自渡之人",
						copywriter: "",
						picUrl: "https://p1.music.126.net/ezt2NwlaFgHbCXJOiCrprA==/109951162899017025.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1683691365428,
						playCount: 56490732,
						trackCount: 223,
						highQuality: false,
						alg: "alg_high_quality"
					},
				],
				imgs2: [{
						id: 691394551,
						type: 0,
						name: "那人那景都将在遗忘中重新拾起",
						copywriter: "",
						picUrl: "https://p2.music.126.net/LmEn2OfY3SbJ96t-FU2_Pw==/109951164026376663.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1632368012178,
						playCount: 28184366,
						trackCount: 98,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 2520739691,
						type: 0,
						name: "纯音乐 轻音乐 解压 学习 刷题 睡觉 御用",
						copywriter: "",
						picUrl: "https://p2.music.126.net/SGD1b-rku41Lj0QATboFrw==/109951166258366024.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1681566010641,
						playCount: 124563208,
						trackCount: 168,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 2748492595,
						type: 0,
						name: "欧美万评优质女声•萦绕耳畔忆于心间",
						copywriter: "",
						picUrl: "https://p2.music.126.net/ptx2Jf4PZl3oNLxv4NiADg==/109951164018765577.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1675992416262,
						playCount: 36467308,
						trackCount: 170,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 2703033645,
						type: 0,
						name: "『1w+热评』欧美万评撩耳男声（单曲循环）",
						copywriter: "",
						picUrl: "https://p2.music.126.net/xLDdcvX4nVVHePy8qcvYVQ==/109951163994703160.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1666931436098,
						playCount: 69031160,
						trackCount: 227,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 2511560749,
						type: 0,
						name: "温柔暴击 | 沉溺于男友音的甜蜜乡",
						copywriter: "",
						picUrl: "https://p2.music.126.net/zlZc45irggToHtzvJaDfLA==/109951164802165973.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1683702220600,
						playCount: 44584892,
						trackCount: 167,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 863956318,
						type: 0,
						name: "50部爱情电影，50种浓情蜜意",
						copywriter: "",
						picUrl: "https://p2.music.126.net/SBEm15YRlBj9vnYQhAimrA==/109951162990572542.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1555234122725,
						playCount: 37356792,
						trackCount: 50,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 123243715,
						type: 0,
						name: "[声线] 空 灵 女 声",
						copywriter: "",
						picUrl: "https://p2.music.126.net/3RANMlMM-udSsHyInyVbrQ==/528865105234307.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1678525624408,
						playCount: 25270268,
						trackCount: 60,
						highQuality: false,
						alg: "alg_high_quality"
					},
					{
						id: 2821115454,
						type: 0,
						name: "[一周原创发现] HorseKing带你预知未来的轨迹",
						copywriter: "",
						picUrl: "https://p2.music.126.net/FiKuwWdLOm4goj1nTn0j6A==/109951168593255445.jpg",
						canDislike: true,
						trackNumberUpdateTime: 1683302400000,
						playCount: 59814220,
						trackCount: 30,
						highQuality: false,
						alg: "alg_high_quality"
					},
				]
			}
		},
		mounted() {
			this.getsonglist()
		},
		methods: {
			async getsonglist() {
				const res = await this.$myRequest({
					url: "/personalized"
				})
				this.imgs2 = res.data.result.slice(5,20)
				this.imgs = res.data.result.slice(0,4)
			}
		},
		computed:{
			formatNum() {
			      return function(num) {
			        if (num > 10000&&num < 100000000) return (num / 10000).toFixed(2) + '万';
					if (num>100000000) return (num/100000000).toFixed(2) + '亿';
			      };
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

		.card {
			.recommend {
				display: flex;
				overflow: auto;

				.one {
					width: 35%;
					position: relative;
					.ico{
					position: absolute;
						top: 5%;
						right: 5%;
					}
				}

				.two {
					width: 65%;
					display: flex;

					.recommend2 {
						position: relative;
						margin-left: 50rpx;
						.ico{
							position: absolute;
							top: 5%;
							right: 5%;
							display: flex;
							align-items: center;
						}
					}
				}
			}
		}
	}
</style>