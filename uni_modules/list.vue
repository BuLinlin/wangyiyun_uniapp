<template>
	<view class="list">
		<view class="litbox" v-for="item in imgs" :key="item.id">
			<image style="background-color:rgb(220, 47, 39);width: 100rpx;height: 100rpx; border-radius: 50%;margin-bottom: 20rpx;" :src="item.iconUrl" mode=""></image>
			<view style="width: 100%;text-align: center;white-space:nowrap;">{{item.name}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return{
				imgs:[
					{
					id: -1,
					name: "每日推荐",
					iconUrl: "http://p1.music.126.net/4DpSgAVpJny4Ewf-Xw_WQQ==/109951163986641971.jpg",
					url: "orpheus://songrcmd",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: -6,
					name: "私人FM",
					iconUrl: "http://p1.music.126.net/Shi7cRT1bDhwpVDM7AOFXg==/109951165265330616.jpg",
					url: "orpheus://privatefm",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: -2,
					name: "歌单",
					iconUrl: "http://p1.music.126.net/uG5p6CnwAHrLqOkaSeRlnA==/109951163986649164.jpg",
					url: "orpheus://playlistCollection",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: -3,
					name: "排行榜",
					iconUrl: "http://p1.music.126.net/SDFC6A3X2wzUCavYyeGIOg==/109951163986649670.jpg",
					url: "orpheus://rnpage?component=rn-ranklist-homepage&mainProcessCompat=1&isTheme=true&split=index",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 1025001,
					name: "有声书",
					iconUrl: "http://p1.music.126.net/Kb4oK0m_ocs3FR3lo-r9yg==/109951167319110429.jpg",
					url: "orpheus://rnpage?component=rn-podcast-book&route=book-home&split=book-home&focusTab=book&mainProcessCompat=1",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 13000,
					name: "数字专辑",
					iconUrl: "http://p1.music.126.net/nRWhsf3P7r7eqHz-v61VBg==/109951166989045593.jpg",
					url: "https://music.163.com/v/m/album/poly/detail",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 11000,
					name: "直播",
					iconUrl: "http://p1.music.126.net/2JvVZZjcjyCE72fGMsC1hg==/109951166989043011.jpg",
					url: "orpheus://playlive?id=29021650&multiProtocolSource=look&multiProtocolLiveType=voicelive&livesource=live_circle&alg=alg_live_maincircle_popularity$79d15ae215bec5606fda9d4f57c848df&ops=abtest%3Alive-main-rk_original%2Cso%3A5.0000.0%2Ctimestamp%3A1683610487650&liveUrl=http%3A%2F%2Fpull0583d674.live.126.net%2Flive%2F018cd2d499f9470597aed67983bdb4cd.flv%3Fnetease%3Dpull0583d674.live.126.net&liveType=2&liveId=67717023&anchorId=346861247&enterRoomAbGroup=t&skipUrls=%5B%22orpheus%3A%2F%2Fplaylive%3Fid%3D29021650%26multiProtocolSource%3Dlook%26multiProtocolLiveType%3Dvoicelive%26livesource%3Dlive_circle%26alg%3Dalg_live_maincircle_popularity%2479d15ae215bec5606fda9d4f57c848df%26ops%3Dabtest%253Alive-main-rk_original%252Cso%253A5.0000.0%252Ctimestamp%253A1683610487650%26liveUrl%3Dhttp%253A%252F%252Fpull0583d674.live.126.net%252Flive%252F018cd2d499f9470597aed67983bdb4cd.flv%253Fnetease%253Dpull0583d674.live.126.net%26liveType%3D2%26liveId%3D67717023%26anchorId%3D346861247%22%2C%22orpheus%3A%2F%2Fplaylive%3Fid%3D481498368%26multiProtocolSource%3Dlook%26multiProtocolLiveType%3Dvoicelive%26livesource%3Dlive_circle%26alg%3Dalg_live_maincircle_popularity%2479d15ae215bec5606fda9d4f57c848df%26ops%3Dabtest%253Alive-main-rk_original%252Cso%253A5.0000.0%252Ctimestamp%253A1683610487650%26liveUrl%3Dhttp%253A%252F%252Fpull0583d674.live.126.net%252Flive%252F8776344b0ce14f53ab9fc9005651eda5.flv%253Fnetease%253Dpull0583d674.live.126.net%26liveType%3D2%26liveId%3D67713065%26anchorId%3D5162884607%22%2C%22orpheus%3A%2F%2Fplaylive%3Fid%3D388954665%26multiProtocolSource%3Dlook%26multiProtocolLiveType%3Dvoicelive%26livesource%3Dlive_circle%26alg%3Dalg_live_maincircle_popularity%2479d15ae215bec5606fda9d4f57c848df%26ops%3Dabtest%253Alive-main-rk_original%252Cso%253A5.0000.0%252Ctimestamp%253A1683610487650%26liveUrl%3Dhttp%253A%252F%252Fpull0583d674.live.126.net%252Flive%252F9bda4cef8c7d4e1b8a92aabbdd8816c7.flv%253Fnetease%253Dpull0583d674.live.126.net%26liveType%3D2%26liveId%3D67724797%26anchorId%3D4012802745%22%2C%22orpheus%3A%2F%2Fplaylive%3Fid%3D121138227%26multiProtocolSource%3Dlook%26multiProtocolLiveType%3Dvoicelive%26livesource%3Dlive_circle%26alg%3Dalg_live_maincircle_popularity%2479d15ae215bec5606fda9d4f57c848df%26ops%3Dabtest%253Alive-main-rk_original%252Cso%253A5.0000.0%252Ctimestamp%253A1683610487650%26liveUrl%3Dhttp%253A%252F%252Fpull0583d674.live.126.net%252Flive%252F2b175e8ae7644408b2007c6b5192cdc6.flv%253Fnetease%253Dpull0583d674.live.126.net%26liveType%3D2%26liveId%3D67716986%26anchorId%3D484993150%22%2C%22orpheus%3A%2F%2Fplaylive%3Fid%3D392842480%26multiProtocolSource%3Dlook%26multiProtocolLiveType%3Dvoicelive%26livesource%3Dlive_circle%26alg%3Dalg_live_maincircle_popularity%2479d15ae215bec5606fda9d4f57c848df%26ops%3Dabtest%253Alive-main-rk_original%252Cso%253A5.0000.0%252Ctimestamp%253A1683610487650%26liveUrl%3Dhttp%253A%252F%252Fflv68ee743a.live.126.net%252Flive%252Fd16cb68f037f4c12a53cc6d0b9f6158d.flv%253Fnetease%253Dflv68ee743a.live.126.net%26liveType%3D2%26liveId%3D67712110%26anchorId%3D4038163270%26anchorWarmAudio%3D%25257B%252522audioUrl%252522%25253A%252522https%25253A%25252F%25252Ff1.iplay.126.net%25252Fobj%25252FwojDmcKVw6rCmD7DjMK_%25252F12000880503%25252F7539%25252Fa220%25252Fd782%25252F32baa8fa12b1f43da1399fc0afa559e0.mp3%252522%25252C%252522duration%252522%25253A10214%25257D%26avatarUrl%3Dhttp%253A%252F%252Fp2.music.126.net%252F_L73s3DB4ax4YMdrqB5iWQ%253D%253D%252F109951168219244199.jpg%26circle_slide%3D1%26circle_title%3D%E5%85%B3%E6%B3%A8%E4%B8%BB%E6%92%AD%22%5D",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 1025000,
					name: "关注新歌",
					iconUrl: "http://p1.music.126.net/BAOWsqZmmxL8JIH-wejMmQ==/109951167294312390.jpg",
					url: "orpheus://rnpage?component=rn-newsong-publish",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 1027000,
					name: "收藏家",
					iconUrl: "http://p1.music.126.net/gk99UFRasebERf38t6A1kA==/109951168168319514.jpg",
					url: "orpheus://miniProgram?appId=62f4d0986bd200f94c847935&source=dragonball",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					},
					{
					id: 18000,
					name: "游戏专区",
					iconUrl: "http://p1.music.126.net/qzKViKyOodgMYIEpp5t1NQ==/109951166989041366.jpg",
					url: "orpheus://rnpage?component=ReactNativeGame&gameSource=mainpage_circle",
					skinSupport: true,
					homepageMode: "RCMD_MODE",
					resourceState: null
					}
				]
			}
		},
		mounted() {
			this.getlist()
		},
		methods:{
		async getlist(){
				const res = await this.$myRequest({
					url:'/homepage/dragon/ball'
				})
				this.imgs = res.data.data
			}
		}
	}
</script>

<style lang="less" scoped>
	::-webkit-scrollbar {
	  display: none; /* Chrome Safari */}
	.list{
		padding-top: 40rpx;
		display: flex;
		flex-wrap: nowrap;
		overflow: auto;
		justify-content: space-between;
		.litbox{
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-items: center;
			margin-left: 5%;
			width: 25%;
		}
	}
</style>