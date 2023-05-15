<template>
	<view class="bigbox">
		<!-- 文字部分 -->
		<view class="ico">
			<van-icon size=20 color=#FB7299 name="play-circle" />
			<span style="font-size: 33rpx;font-weight: bold;">播放全部</span>
		</view>
		<!-- 列表部分 -->
		<view class="list" v-for="item in dailySongs" :key="item.id">
			<image :src=item.al.picUrl mode="" style="width: 100rpx;height: 100rpx;border-radius: 10rpx;"></image>
			<view class="span">
				<span>{{item.name}}</span>
				<view class="introduce">
					<van-tag type="primary">{{item.reason}}</van-tag>
					<span>{{item.alia[0]}}</span>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				dailySongs: [{
					name: "爱殇",
					id: 1332153723,
					pst: 0,
					t: 0,
					ar: [{
						id: 12079173,
						name: "小时姑娘",
						tns: [],
						alias: []
					}],
					alia: [
						"电视剧《东宫》插曲"
					],
					pop: 100,
					st: 0,
					rt: null,
					fee: 8,
					v: 349,
					crbt: null,
					cf: "",
					al: {
						id: 74800935,
						name: "爱殇",
						picUrl: "http://p3.music.126.net/U8gz-goWF6O0KNWxAQN01Q==/109951163870763627.jpg",
						tns: [],
						pic_str: "109951163870763627",
						pic: 109951163870763630
					},
					dt: 304175,
					h: {
						br: 320000,
						fid: 0,
						size: 12169970,
						vd: -49779,
						sr: 44100
					},
					m: {
						br: 192000,
						fid: 0,
						size: 7302000,
						vd: -47168,
						sr: 44100
					},
					l: {
						br: 128000,
						fid: 0,
						size: 4868014,
						vd: -45460,
						sr: 44100
					},
					sq: {
						br: 892549,
						fid: 0,
						size: 33936502,
						vd: -49779,
						sr: 48000
					},
					hr: null,
					a: null,
					cd: "01",
					no: 1,
					rtUrl: null,
					ftype: 0,
					rtUrls: [],
					djId: 0,
					copyright: 2,
					s_id: 0,
					mark: 64,
					originCoverType: 1,
					originSongSimpleData: null,
					tagPicList: null,
					resourceState: true,
					version: 349,
					songJumpInfo: null,
					entertainmentTags: null,
					single: 0,
					noCopyrightRcmd: null,
					rtype: 0,
					rurl: null,
					mst: 9,
					cp: 0,
					mv: 0,
					publishTime: 1544274133830,
					reason: "超76%人播放",
					recommendReason: "超76%人播放",
					privilege: {
						id: 1332153723,
						fee: 8,
						payed: 0,
						st: 0,
						pl: 128000,
						dl: 0,
						sp: 7,
						cp: 1,
						subp: 1,
						cs: false,
						maxbr: 999000,
						fl: 128000,
						toast: false,
						flag: 258,
						preSell: false,
						playMaxbr: 999000,
						downloadMaxbr: 999000,
						maxBrLevel: "lossless",
						playMaxBrLevel: "lossless",
						downloadMaxBrLevel: "lossless",
						plLevel: "standard",
						dlLevel: "none",
						flLevel: "standard",
						rscl: null,
						freeTrialPrivilege: {
							resConsumable: false,
							userConsumable: false,
							listenType: 0
						},
						chargeInfoList: [{
								rate: 128000,
								chargeUrl: null,
								chargeMessage: null,
								chargeType: 0
							},
							{
								rate: 192000,
								chargeUrl: null,
								chargeMessage: null,
								chargeType: 1
							},
							{
								rate: 320000,
								chargeUrl: null,
								chargeMessage: null,
								chargeType: 1
							},
							{
								rate: 999000,
								chargeUrl: null,
								chargeMessage: null,
								chargeType: 1
							}
						]
					},
					alg: "play_itembased_on"
				}],
			}
		},
		created() {
			
		},
		mounted() {
			this.emit()
		},
		methods:{
			emit(){
				this.$emit('day',this.dailySongs[0].al.picUrl)
			}
		}
	}
</script>

<style lang="less" scoped>
	.bigbox{
		padding: 5%;
		.ico{
			display: flex;
			align-items: center;
			margin-bottom: 5%;
			span{
				margin-left: 2%;
			}
		}
		.list{
			display: flex;
			width: 100%;
			height: 100rpx;
		}
	}
</style>