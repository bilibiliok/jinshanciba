<template>
	<div class="home-download">
		<div class="home-download-content">
			<img src="../../../assets/image/ciba-icon.png" alt="">
			<h1>金山词霸</h1>
			<p>多端数据云端同步，支持多个设备</p>
			<p>拍照语音翻译，支持英法日等7国语音</p>
			<ul>
				<li @mouseenter="showMessage" @mouseleave="hiddenMessage">
					<div>
						<img src="//cdn.iciba.com/www/img/www/0312/apple-icon.png" alt=""> iPhone版下载<a href="//cp.iciba.com/mobile"></a>
					</div>
					<div v-show="showPicture">
						<p>手机直接扫码下载</p>
						<img src="//cdn.iciba.com/www/img/www/0312/ios-qrcode.png" alt="">
					</div>
				</li>
				<li @mouseenter="showMessage1" @mouseleave="hiddenMessage1">
					<div>
						<img src="//cdn.iciba.com/www/img/www/0312/android-icon.png" alt=""> Android版下载<a href="//cp.iciba.com/mobile"></a>
					</div>
					<div v-show="showPicture1">
						<p>手机直接扫码下载</p>
						<img src="//cdn.iciba.com/www/img/www/0312/android-qrcode-new.png" alt="">
					</div>
				</li>
			</ul>
		</div>
	</div>
</template>
<script>
export default {
	data() {
		return {
			showPicture: false,
			showPicture1: false
		}
	},
	methods:{
		showMessage() {
			this.showPicture = true
		},
		showMessage1() {
			this.showPicture1 = true
		},
		hiddenMessage() {
			this.showPicture = false
		},
		hiddenMessage1() {
			this.showPicture1 = false
		}

	}
}
</script>
<style scoped>
	.home-download{
		width: 1200px;
		margin: 0 auto;
		background: url(//cdn.iciba.com/www/img/www/0312/dl-bg.jpg) no-repeat;
		background-size: 100% 100%;
		height: 480px;
		margin-top: 20px;
		position: relative;
		z-index: 1
	}
	.home-download-content{
		text-align: center;
		line-height: 1.4;
		position: absolute;
		top: 120px;
		left: 85px
	}
	.home-download-content h1{
		font-size: 30px;
		color: #222;
		margin: 6px auto 10px
	}
	.home-download-content p{
		color: #666
	}
	.home-download-content ul{
		margin-top: 20px;
	}
	.home-download-content ul li{
		margin: 0 5px;
		width: 180px;
		/* height: 50px; */
		cursor: pointer;
		line-height: 50px;
		display: inline-block;
		overflow: hidden;
		vertical-align: top
	}
	.home-download-content ul li div:first-child{
		color: #fff;
		background: #111;
		position: relative;
		
	}
	.home-download-content ul li div:first-child:hover{
		background: lightblue
	}
	.home-download-content ul li img{
		width: 30px;
		height: 30px;
		vertical-align: middle
	}
	.home-download-content ul li div:last-child{
		background: #fff;
		margin-top: 10px;
		padding: 10px;
		border: 1px solid #ededed;
		border-radius: 1px
	}
	.home-download-content ul li div:last-child img{
		width: 140px;
		height: 140px
	}
</style>