<template>
	<view>
		<van-nav-bar :title="title"  left-arrow fixed :left-arrow="back" @click-left="handleBack">
			<template v-if="!back" #left>
				<slot name="left" />
			</template>
			<template v-if="!titie" #title>
				<slot name='title'></slot>
			</template>
			<template #right>
				<slot name='right'></slot>
			</template>
		</van-nav-bar>
	</view>
</template>

<script>
	export default {
		props: ['back'],
		data() {
			return {

			};
		},
		onLoad() {

		},
		mounted() {
			console.log(this.back)
		},
		methods: {
			handleBack() {
				if (this.back) {
					un.navigateBack()
				}
			}
		}
	}
</script>

<style lang="less" scoped>

</style>