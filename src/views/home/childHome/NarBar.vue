<template>
	<div class="nar-bar" ref="searchBar">
		<div class="nav-content">
			<ul class="nav-content-left" v-show="isShow">
				<li class="active">首页</li>
				<li>背单词</li>
				<li>双语美文</li>
				<li>练听力</li>
				<li>文档翻译</li>
				<li>人工翻译</li>
			</ul>
			<ul  class="nav-content-right">
				<!-- :class="topHeight" -->
				<li><a href="">客户端下载</a></li>
				<li><a href="">专栏平台</a></li>
				<div class="nar-content-user">
					<img src="../../../assets/image/user.png" alt="">
				</div>
			</ul>
			
		</div>
		
	</div>
</template>
<script>
export default {
	data() {
		return {
			
		}
	},
	props:{
		isShow:{
			type :Boolean
		}
	}
}
</script>
<style scoped>
	.nar-bar {
		min-width: 1200px;
		margin: 0 auto;
		height: 50px;
		line-height: 50px;
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 99
	}
	.nav-content>ul>li:hover {
		color: #fff;
	}
	.nav-content{
		/* float: right;
		padding: 0 20px; */
		width: 1200px;
		margin: 0 auto;
		padding: 0 20px
	}
	.nav-content ul{
		display: inline-block
	}
	.active{
		color: #fff;
		font-weight: 600
	}
	.nav-content ul>li{
		cursor: pointer;
		margin-right: 40px;
		display: inline-block;
	}
	.nav-content-right{
		float: right;
	}
	.nar-content-user{
		display: inline-block;
		margin-top: 10px;
		vertical-align: -webkit-baseline-middle;
	}
	a{
		color: hsla(0,0%,100%,.6);
	}
	a:hover{
		color: #fff
	}
	
	
	


</style>