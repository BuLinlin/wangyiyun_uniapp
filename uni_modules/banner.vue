<template>
	<view class="uni-margin-wrap">
		<swiper class="swiper" circular indicator-dots="true" :autoplay="autoplay" :interval="interval"
			:duration="duration">
			<swiper-item v-for="item in imgs" :key="item.index">
				<image :src="item.pic" mode="" style="width: 100%; height: 100%;"></image>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgs: [{
					pic: 'http://p1.music.126.net/Wn2rUBaIjzgRNZAw3jO4nQ==/109951168600686089.jpg'
				},{
					pic:'http://p1.music.126.net/h3d-bmC_eNVaJZogMhqH4w==/109951168600644471.jpg'
				}]
			}
		},
		mounted() {
			this.getbanner()
			console.log('111')
		},
		methods: {
			async getbanner() {
				const res = await this.$myRequest({
					url: '/banner?type=2'
				})
				this.imgs = res.data.banners
			}
		}
	}
</script>

<style lang="less" scoped>
	.uni-margin-wrap {
		margin-top: 80rpx;
	}
</style>