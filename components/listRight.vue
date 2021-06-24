<template>
	<view class="listright">
		<view class="author-img">
			<image class="img" src="../static/img/t.png" mode=""></image>
			<image src="../static/img/+.png" mode="" class="add" v-if="show" @click="hide"></image>
			
		</view>
		<view class="iconfont iconaixin right-box" :style="color" @click="changeColor">
		</view>
		<image src="../static/img/ax.png" mode="" class="right-box"></image>
		<view class="number">
			12.3w
		</view>
		<view class="number">
		</view>
		<image src="../static/img/fx.png" mode="" class="right-box"></image>
		<view class="number">
			234
		</view>
		<view class="around">
			<image class="img" src="../static/img/cp.png" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				show:true,
				color:''
			};
		},
		methods:{
			hide(){
				this.show=!this.show		
			},
			changeColor(){
				this.color=this.color===''?"color:red;":''
			}
		}
	}
</script>

<style>
.listright{
	width: 50px;
	margin: 0 auto;
}
.author-img{
	width: 50px;
	height: 50px;
	border-radius: 50%;
	border: 2px solid #FFFFFF;
	position: relative;
}
.img{
	width: 50px;
	height: 50px;
	border-radius: 50%;
}
.right-box{
	width: 45px;
	height: 45px;
	text-align: center;
	line-height: 40px;
	color: #FFFFFF;
	font-size: 33px;
	margin: 8px 2px;
}
.number{
	font-size: 10px;
	text-align: center;
	color: #FFFFFF;
}
.around{
	width: 50px;
	height: 50px;
	margin:15px auto;
	animation: rotate 1.5s linear 0.2s infinite;
}
.add{
	width: 18px;
	height: 18px;
	border-radius: 50%;
	background: red;
	position: absolute;
	bottom: -9px;
	left: 16px;
	text-align: center;
	line-height: 18px;
	color: #FFFFFF;
	font-size: 10px;
}
/* 右侧播放动画 */
@keyframes ratate{
	0%{
		transform: rotate(0deg)
	}
	100%{
		transform: rotate(360deg);
	}
}
</style>