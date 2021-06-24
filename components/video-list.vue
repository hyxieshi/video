<template>
	<view class="videoList">
		<view class="video">
			<view class="swiper-box">
				<swiper class="swiper" :vertical="true" @touchstart="touchStart" @touchend="touchEnd">
					<!-- 如果后台 传过来的值有唯一的id  key 尽量绑定唯一的id -->
					<swiper-item v-for="(item,i) of videolist" :key="i">
						<!-- <swiper-item> -->
						<view class="swiper-item">
							<view class="videoPlayer">
								<!-- 在wx 小程序中  视频地址需要是网络地址 本地的视频是渲染不了的-->
								<video id="myVideo" class="video" :src="`../../static/video/video (${item}).mp4`"
									:autoplay="true" :loop="true"></video>
							</view>
						</view>
						<view class="left-box">
							<list-left></list-left>
						</view>
						<view class="right-box">
							<list-right></list-right>
						</view>
					</swiper-item>
				</swiper>
			</view>
		</view>
	</view>
</template>


<script>
	import listLeft from './listLeft.vue'
	import listRight from './listRight.vue'
	export default {
		name: "video-list",
		data() {
			return {
				// 这里 可以使用request 请求数据赋值给list 通过for 渲染
				videolist: ['1', '2', '3', '4', '5', '6', '7', '8', '9']
			};
		},
		components:{
			listLeft,listRight
		},
		methods: {
			// 监听滑动（上下）
			//  获取 触碰开始 结束的位置来 设置视频是否暂停 播放
			touchStart(res) {
				this.pageStartY = res.changedTouches[0].pageY
			},
			touchEnd(res) {
				this.pageStartY = res.changedTouches[0].pageY
			}
		}
	}
</script>

<style>
	.videoPlayer {
		width: 100%;
		height: 100%;
	}

	.video {
		width: 100%;
		height: 100vh;
	}

	.videoList {
		width: 100%;
		height: 100%;
	}

	.swiper-box {
		width: 100%;
		height: 100%;
	}

	.swiper {
		width: 100%;
		height: 100%;
	}

	.swiper-item {
		width: 100%;
		height: 100%;
		z-index: 19;
	}

	.left-box {
		z-index: 20;
		position: absolute;
		bottom: 50px;
		left: 10px;
	}

	.right-box {
		z-index: 20;
		position: absolute;
		bottom: 50px;
		right: 10px;
	}
</style>
