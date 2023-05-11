<template>
	<view class="bigbox">
		<view class="onebox">
			<span style="font-size: 33rpx;font-weight: bold;">推荐新音乐<van-icon name="arrow" /></span>
		</view>
		<view class="twobox">
			<swiper :indicator-dots="flase" :autoplay="flase" :interval="3000" :duration="1000"  style="height: 350rpx;">
				<swiper-item v-for="(item,index) in grouped" :key="grouped.index">
					<view class="swiper-item"" v-for="list in item" :key="list.id">
						<image :src="list.picUrl" mode="" style="width: 100rpx;height: 100rpx;border-radius: 20rpx;"></image>
						<span style="width: 80%;">{{list.copywriter}}</span>
					</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						id: 14514232,
						url: "",
						picUrl: "https://p2.music.126.net/ZfQoqzo0rTqe3sFKkDnGuw==/109951167211930348.jpg",
						sPicUrl: "https://p2.music.126.net/xLa1qgy1Mu3wRXFZ3GNLiA==/109951167211942016.jpg",
						type: 5,
						copywriter: "《超级面对面》第254期 keshi：我的音乐永远新鲜",
						name: "《超级面对面》第254期 keshi：我的音乐永远新鲜",
						time: 1648546294107
					},
					{
						id: 14502289,
						url: "",
						picUrl: "https://p2.music.126.net/11GImNvQQkOYFeQsReyyMQ==/109951167063057575.jpg",
						sPicUrl: "https://p2.music.126.net/72JkTBTmLllSenSlQYaO7Q==/109951167063050731.jpg",
						type: 5,
						copywriter: "《超级面对面》第253期 Charlie Puth：灵感就在开关之间",
						name: "《超级面对面》第253期 Charlie Puth：灵感就在开关之间",
						time: 1645107940262
					},
					{
						id: 14498287,
						url: "",
						picUrl: "https://p2.music.126.net/bXBBCrVEKtMZCnAwA8bnXQ==/109951166995281428.jpg",
						sPicUrl: "https://p2.music.126.net/z_XrKvWDuk2Na6LniN3hGA==/109951166995281863.jpg",
						type: 5,
						copywriter: "惊喜呈现| 姜贞羽：热爱舞台上的每一个瞬间",
						name: "惊喜呈现| 姜贞羽：热爱舞台上的每一个瞬间",
						time: 1643443660577
					},
					{
						id: 14495768,
						url: "",
						picUrl: "https://p2.music.126.net/quOJOo3nZ984XzHQYxoJ0w==/109951166983027523.jpg",
						sPicUrl: "https://p2.music.126.net/7LVq4AnJCMPrMhN-PYP28A==/109951166983028013.jpg",
						type: 5,
						copywriter: "惊喜呈现：Yamy郭颖携手二手玫瑰玩转港味复古风",
						name: "惊喜呈现：Yamy郭颖携手二手玫瑰玩转港味复古风",
						time: 1643188917119
					},
					{
						id: 14496631,
						url: "",
						picUrl: "https://p2.music.126.net/IVEDKgbd--myWBukXgreNg==/109951166983018052.jpg",
						sPicUrl: "https://p2.music.126.net/lx35fbctK2npbgPUwt2FXw==/109951166983009311.jpg",
						type: 5,
						copywriter: "《超级面对面》第252期 Alan Walker：和Walkers一起遨游宇宙",
						name: "《超级面对面》第252期 Alan Walker：和Walkers一起遨游宇宙",
						time: 1643188766660
					},
					{
						id: 14494332,
						url: "",
						picUrl: "https://p2.music.126.net/3VcZPjsmzKYUgTTTb9vkzg==/109951166978021312.jpg",
						sPicUrl: "https://p2.music.126.net/z4p7TB8jdjtVQdLZhi7YNw==/109951166978019826.jpg",
						type: 5,
						copywriter: "《乐评故事》根据《删了吧》改编情感故事",
						name: "《乐评故事》根据《删了吧》改编情感故事",
						time: 1643087773587
					},
					{
						id: 14493009,
						url: "",
						picUrl: "https://p2.music.126.net/wlX0LLvcsgD9g2NMOOiffA==/109951166952951891.jpg",
						sPicUrl: "https://p2.music.126.net/BZ6klU2ZST26naXNw6-2lQ==/109951166952947483.jpg",
						type: 5,
						copywriter: "《超级面对面》第251期 吴建豪：在舞台上真实的发光",
						name: "《超级面对面》第251期 吴建豪：在舞台上真实的发光",
						time: 1642569097449
					},
					{
						id: 14492088,
						url: "",
						picUrl: "https://p1.music.126.net/MvXrmjA6WuyrMbBU9wdPzg==/109951166952526945.jpg",
						sPicUrl: "https://p1.music.126.net/6igO12W7o95H9Up_5-zurQ==/109951166952527990.jpg",
						type: 5,
						copywriter: "《乐评故事》EP07：最美好的爱情",
						name: "《乐评故事》EP07：最美好的爱情",
						time: 1642564464501
					},
					{
						id: 14486290,
						url: "",
						picUrl: "https://p1.music.126.net/uaCZRvnB7n7LccGlfhjOZw==/109951166871788716.jpg",
						sPicUrl: "https://p1.music.126.net/zaqRpOh5pEbgZL4EOatU1A==/109951166871786323.jpg",
						type: 5,
						copywriter: "《乐评故事》EP05：不想停止爱你这件事",
						name: "《乐评故事》EP05：不想停止爱你这件事",
						time: 1640239400353
					}
				], // 从后端获取到的数据
				grouped: [] // 分组后的数据存储数组
			}
		},
		computed: {
			groupedData() {
				const groups = [];
				for (let i = 0; i < this.list.length; i += 3) {
					groups.push(this.list.slice(i, i + 3));
				}
				this.grouped = groups;
				return this.grouped;
			}
		},
		mounted() {
			// 从后端获取数据并存储到list数组中
			this.getrecomlist()
			console.log(this.grouped)
		},
		methods:{
			async getrecomlist(){
				const res = await this.$myRequest({
					url:"/personalized/privatecontent/list?limit=9"
				})
				console.log(res.data.result)
				this.list = res.data.result
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
		.twobox{
			.swiper-item{
				display: flex;
				margin-bottom: 3%;
				justify-content: space-between;
				align-items: center;
			}
		}
	}
</style>