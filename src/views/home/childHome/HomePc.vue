<template>
	<div class="home-pc">
		<ul>
			<li>
				<img src="//cdn.iciba.com/www/img/www/0312/win-icon.png" alt="">
				<h3>PC版个人版下载</h3>
				<p>准确、便捷的查词翻译软件</p>
				<em>查看更多 ></em>
				<a href="//cp.iciba.com/"></a>
			</li>
			<li><img src="//cdn.iciba.com/www/img/www/0312/mac-icon.png" alt="">
				<h3>PC版企业版下载</h3>
				<p>准确、便捷的查词翻译软件</p>
				<em>查看更多 ></em>
				<a href="//cp.iciba.com/pc-company/"></a>
			</li>
			<li>
				<img src="//cdn.iciba.com/www/img/www/0312/ios-icon.png" alt="">
				<h3>Mac版版下载</h3>
				<p>准确、便捷的查词翻译软件</p>
				<em>查看更多 ></em>
				<a href="//cp.iciba.com/mac/"></a>
			</li>
		</ul>
	</div>
</template>
<script>
export default {
	data() {
		return {

		}
	}
}
</script>
<style scoped>
	.home-pc{
		width: 1200px;
		margin: 0 auto;
		margin-top: 20px;
		padding-bottom: 50px;
	}
	.home-pc ul li{
		width: 386px;
		height: 310px;
		position: relative;
		background: #fff;
		display: inline-block;
		cursor: pointer;
		text-align: center;
		box-sizing: border-box;
		padding-top: 43px;
		line-height: 1.4;
		margin-right: 21px;
	}
	.home-pc ul li:last-child{
		margin-right:0
	}
	.home-pc ul li>img{
		width: 110px;
		height: 110px
	}
	.home-pc ul li>h3{
		font-size: 22px;
		margin-top: 30px;
		color: #222;
	}
	.home-pc ul li>p{
		color: #999;
		margin-top: 6px;
	}
	.home-pc ul li>em{
		color: #0288fb;
		margin-top: 7px;
	}
	.home-pc ul li>a{
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0
	}
	.home-pc ul li:hover{
		box-shadow: 0 10px 10px 0 rgba(0,0,0,.1);
	}
	
</style>