<template>
	<view class="bigbox">
		<!-- 轮播图 -->
		<view class="banner">
			<image :src=banner mode="" style="width: 100%;height: 100%;"></image>
			<view class="day">
				<span class="sp1">{{date.sun}}</span>
				<span class="sp2">/{{date.moon}}</span>
			</view>
		</view>
		<!-- 列表 -->
		<songlist @day="getday()"></songlist>
	</view>
</template>

<script>
	import songlist from "@/uni_modules/Song_List.vue"
	export default {
		components: {
			songlist
		},
		data() {
			return {
				date: {
					moon: '',
					sun: ''
				},
				banner:''
			};
		},
		onLoad(b) {
			uni.setNavigationBarTitle({
				title: b.name
			});
			this.getdate()
		},
		methods: {
			getdate() {
				const daily = new Date();
				const day = daily.getDate();
				let month = daily.getMonth();
				if(month>=1 && month<=9){
					month = '0' + month
				}
				this.date.sun = day;
				this.date.moon = month
			},
			getday(img){
				this.banner = img
			}
		}
	}
</script>

<style lang="less" scoped>
.bigbox{
	.banner{
		height: 25vh;
		position: relative;
		.day{
			position: absolute;
			left: 5%;
			top: 80%;
			color: #fff;
			.sp1{
				font-size: 40rpx;
				font-weight: bold;
			}
		}
	}
}
</style>