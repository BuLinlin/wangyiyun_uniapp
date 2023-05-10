<template>
	<view class="content">
		<myheader :back=false>
			<template #left>
				<van-icon size="35rpx" name="wap-nav" />
			</template>
			<template #title>
				<van-search :value="value" :placeholder=placeholder custom-class="width:100%" />
			</template>
			<template #right>
				<van-icon size="35rpx" name="bell" />
			</template>
		</myheader>
		<mybanner></mybanner>
		<mylist></mylist>
		<!-- 推荐歌单 -->
		<songlist></songlist>
		<view class="van-hairline--top"></view>
		111
	</view>
</template>

<script>
	import myheader from '@/uni_modules/header/header.vue'
	import mybanner from '@/uni_modules/banner.vue'
	import mylist from '@/uni_modules/list.vue'
	import songlist from "@/uni_modules/song_sheet.vue"
	export default {
		components: {
			myheader,
			mybanner,
			mylist,
			songlist
		},
		data() {
			return {
				value: '',
				placeholder: '请输入关键词',
			}
		},
		onLoad() {
			this.getSearch()
		},
		onShow() {},
		methods: {
			// 获取搜索框数据
			async getSearch() {
				const res = await this.$myRequest({
					url: '/search/default'
				})
				this.placeholder = res.data.data.showKeyword
			}
		}
	}
</script>

<style lang="less" scoped>
</style>