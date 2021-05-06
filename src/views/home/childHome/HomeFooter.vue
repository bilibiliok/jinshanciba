<template>
	<div class="footer">
		<ul class="footer-content">
			<li>
				<img src="//cdn.iciba.com/www/img/www/0312/phone.png" alt="">
				<h3>致电销售顾问</h3>
				<p>拨打我们的电话，与经验丰富的销售顾问交流</p>
				<h5>13511035060</h5>
			</li>
			<li>
				<img src="//cdn.iciba.com/www/img/www/0312/mail.png" alt="">
				<h3>电子邮件咨询</h3>
				<p>发邮件至我们的邮箱，我们将尽快为您答疑解惑</p>
				<h5>kcb_kf@kingsoft.com</h5>
			</li>
		</ul>
		<h5 class="footer-record">
			<img src="http://dict-pc.kss.ksyun.com/public-icons/guohui.png" alt="" class="footer-guohui">
			京ICP备14035597号-3 站长统计
		</h5>
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
	.footer{
		min-width: 1200px;
		width: 100%;
		background: #26262a;
	}
	.footer ul{
		margin: 0 auto;
		width: 1200px;
	}
	.footer ul li{
		display: inline-block;
		padding: 50px 0;
		text-align: center;
		width: 50%;
		line-height: 1.4
	}
	.footer ul li>img{
		width: 34px;
		height: 34px;
	}
	.footer ul li>h3{
		font-size: 20px;
		color: hsla(0, 0%, 100%, .4);
		margin-top: 20px
	}
	.footer ul li>p{
		color: hsla(0, 0%, 100%, .4);
		margin-top: 4px;
	}
	.footer ul li h5{
		color: #fff;
		font-size: 20px;
		margin-top: 6px
	}
	.footer-record{
		color: hsla(0,0%,100%,.2);
		line-height: 40px;
		background-color: #1a1b1d;
		text-align: center
	}
	.footer-guohui{
		vertical-align: sub;
		transform: translateY(2px)
	}
</style>