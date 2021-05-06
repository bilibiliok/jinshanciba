<template>
	<div class="home">
		<home-banner :isType="isType" :isType2="isType2">
			<nar-bar :isShow="isShow" :class="{orderFullScreen:isShow}"></nar-bar>
			<home-banner-content @changeType="changeType"></home-banner-content>
			<home-func></home-func>
			<home-download></home-download>
			<home-pc></home-pc>
			<home-footer></home-footer>
		</home-banner>
	</div>
</template>
<script>
import HomeBanner from './childHome/HomeBanner'
//  引入，首页导航栏
import NarBar from './childHome/NarBar'
// 引入，首页标题查询
import HomeBannerContent from './childHome/HomeBannerContent'
// 引入，功能选择
import HomeFunc  from './childHome/HomeFunc'
// 引入下载方式
import HomeDownload from './childHome/HomeDownload';
// 引入pc端下载方式
import HomePc from './childHome/HomePc'
// 引入底部页面
import HomeFooter from './childHome/HomeFooter'
export default {
	components:{
		HomeBanner,
		NarBar,
		HomeBannerContent,
		HomeFunc,
		HomeDownload,
		HomePc,
		HomeFooter
	},
	data() {
		return {
			isType: '',
			isType2: '',
			narSetheight: '',
			scrollTop: '',
			topheight:'',
			isShow: false
		}
	},
	mounted() {
	//监听页面滚动事件
		// this.scrollTop = window.document.documentElement.scrollTop
		window.addEventListener('scroll', this.scrollHandle) // 绑定页面的滚动事件
	//注意：如果由于自己的vue中的样式导致监听不到，可以尝试监听body或者'#app-root'的滚动事件
	},
	watch:{
		
	},
	// computed:{
	// 	topHeight() {
	// 		return window.document.documentElement.scrollTop
	// 	}
	// },
	methods: {
		changeType(type) {
			console.log(type);
			this.isType = type.type1
			this.isType2 = type.type2
		},
		// 监听滚轮高度
		
		// 获取滚动条高度
		scrollHandle(event) {
			// console.log('222111',event);
			let top = event.srcElement.scrollingElement.scrollTop
			this.topheight = top
			// console.log('22222',top);
			if(top >442) {
				this.isShow = true
			} else{
				this.isShow = false
			}
			
		}
	},
}
</script>
<style scoped>
	.home{
		background: #f6f6f6;
		min-width: 1200px;
		height: 100%;
		/* min-height: 1000px */
	}
	.orderFullScreen{
		background-color: rgb(38, 40, 42);
		color: hsla(0,0%,100%,.6);
	}
	@keyframes fadeIn {
		0% {
		opacity: 0; /*初始状态 透明度为0*/
		}
		50% {
		opacity: 0.5; /*中间状态 透明度为0*/
		}
		100% {
		opacity: 1; /*结尾状态 透明度为1*/
	
		}
	}
	.orderFullScreen{
		animation-name: fadeIn; /*动画名称*/
		animation-duration: 3s; /*动画持续时间*/
		animation-iteration-count: 1; /*动画次数*/
		animation-delay: 0s; /*延迟时间*/
	}
</style>