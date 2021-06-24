<template>
	<view class="listLeft">
		<view class="author">
			这里是标题
		</view>
		<view class="title">
			这里是详情说明
		</view>
		<view class="box">
			<view class="music">
				这里是音乐信息
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style scoped>
.listLeft{
	height: 150px;
	margin-left: 10px;
	color: #FFFFFF;
	width: 150px;
	z-index: 21;
}
.author{
	height: 35px;
	line-height: 35px;
	font-size: 15px;
}
.title{
	width: 100%;
	word-wrap: break-word;
	line-height: 22px;
	font-size: 12px;
}
.box{
	width: 100px;
	overflow: hidden;
}
.music{
	width: 140px;
	height: 35px;
	line-height: 35px;
	font-size: 12px;
	animation: music 4s linear 0.2 infinite;
}
/* 左侧文字滚动动画 */
@keyframes music{
	0%{
		transform: translate3d(80%,0,0);
	}
	100%{
		transform: translate3d(-80%,0,0);
	}
}