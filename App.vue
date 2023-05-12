<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	@import 'wxcomponents/@vant/weapp/common/index.wxss';
	/*每个页面公共css */
	body{
		background-color: rgb(245, 245, 245);
	}
	::-webkit-scrollbar {
	  display: none; /* Chrome Safari */}
.van-nav-bar__content{
	display: flex;
	align-items: center;
	overflow: hidden;
}
.van-nav-bar__title{
	max-width: 100% !important;
	width: 80%;
}
</style>
