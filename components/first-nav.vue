<template>
	<view class="firstnav">
		<view class="scrch">
			搜索
		</view>
		<view class="middle">
			<view class="text">
				推荐
			</view>
			<view class="text">
				同城
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"first-nav",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.firstnav{
	position: fixed;
	top: 25px;
	width: 100%;
	height: 40px;
	line-height: 35px;
	margin: 0 auto;
	background: #000000;
	color: #C0C0C0;
	z-index: 21;
	/* display: flex;
	justify-content: space-between; */
}
.scrch{
	display: inline;
	margin-left: 20px;
	}
.middle{
	text-align: center;
	display: inline;
	margin-left:100px;
}
.text{
	display: inline;
	color: #FFFFFF;
	font-size: 20px;
	margin: 0 10px;
}
</style>
