<template>
	<view class="tab">
		<view class="tab-box">
			首页
		</view>
		<view class="tab-box">
			关注
		</view>
		<view class="tab-box">
			加号
		</view>
		<view class="tab-box">
			聊天
		</view>
		<view class="tab-box">
			账号
		</view>
	</view>
</template>

<script>
	export default {
		name:"tab",
		data() {
			return {
				
			};
		}
	}
</script>

<style scoped>
.tab{
	position: absolute;
	height: 50px;
	width: 100%;
	bottom: 0;
	left: 0;
	display: flex;
	justify-content: space-between;
	z-index: 21;
	}
.tab-box{
	flex: 1;
	text-align: center;
}
</style>
