<template>
	<view class="content">
		<first-nav></first-nav>
		<video-list></video-list>
		<tab ></tab>
	</view>
</template>

<script>
	import tab from '../../components/tab.vue'
	import firstNav from '../../components/first-nav.vue'
	import videoList from '../../components/video-list.vue'
	export default {
		data() {
			return {
				
			}
		},
		components:{
			tab,
			firstNav,
			videoList
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
.content{
	height: 100%;
	width: 100%;
}
</style>
