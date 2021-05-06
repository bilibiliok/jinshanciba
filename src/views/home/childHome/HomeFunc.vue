<template>
	<div class="home-func">
		<ul>
			<li  @mouseenter="showActive(1)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 1" src="//cdn.iciba.com/www/img/www/0312/funclist/1a.png" alt="">
				<img v-show="active === 1" src="//cdn.iciba.com/www/img/www/0312/funclist/1b.png" alt="">
				<div>
					<h5 >背单词</h5>
					<p >覆盖117本考试词表</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(2)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 2" src="//cdn.iciba.com/www/img/www/0312/funclist/2a.png" alt="">
				<img v-show="active === 2" src="//cdn.iciba.com/www/img/www/0312/funclist/2b.png" alt="">
				<div>
					<h5 >双语美文</h5>
					<p >了解全球性的窗口</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(3)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 3" src="//cdn.iciba.com/www/img/www/0312/funclist/3a.png" alt="">
				<img v-show="active === 3" src="//cdn.iciba.com/www/img/www/0312/funclist/3b.png" alt="">
				<div>
					<h5 >练听力</h5>
					<p >VOC、BBC在线收听</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(4)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 4" src="//cdn.iciba.com/www/img/www/0312/funclist/4a.png" alt="">
				<img v-show="active === 4" src="//cdn.iciba.com/www/img/www/0312/funclist/4b.png" alt="">
				<div>
					<h5 >说口语</h5>
					<p >每日一练说地道口语</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(5)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 5" src="//cdn.iciba.com/www/img/www/0312/funclist/5a.png" alt="">
				<img v-show="active === 5" src="//cdn.iciba.com/www/img/www/0312/funclist/5b.png" alt="">
				<div>
					<h5 >文档翻译</h5>
					<p >Word、Excel智能翻译 </p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(6)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 6" src="//cdn.iciba.com/www/img/www/0312/funclist/6a.png" alt="">
				<img v-show="active === 6" src="//cdn.iciba.com/www/img/www/0312/funclist/6b.png" alt="">
				<div>
					<h5 >证件翻译</h5>
					<p >身份证、驾驶证等人工翻译</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(7)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 7" src="//cdn.iciba.com/www/img/www/0312/funclist/7a.png" alt="">
				<img v-show="active === 7" src="//cdn.iciba.com/www/img/www/0312/funclist/7b.png" alt="">
				<div>
					<h5 >简历翻译</h5>
					<p >求职简历人工翻译  </p>
				</div>
				<div class="home-func-mask"></div>
			</li>
			<li  @mouseenter="showActive(8)" @ @mouseleave="showActive(0)">
				<img v-show="active !== 8" src="//cdn.iciba.com/www/img/www/0312/funclist/8a.png" alt="">
				<img v-show="active === 8" src="//cdn.iciba.com/www/img/www/0312/funclist/8b.png" alt="">
				<div>
					<h5 >论文翻译</h5>
					<p >毕业论文人工翻译</p>
				</div>
				<div class="home-func-mask"></div>
			</li>
		</ul>
	</div>
</template>
<script>
export default {
	data() {
		return {
			active: 0
		}
	},
	methods:{
		showActive(index) {
			this.active = index
		}
	}
}
</script>
<style scoped>
	.home-func{
		width: 1200px;
		margin: 0 auto;
		box-sizing: border-box;
		padding: 20px 0 20px 40px;
		background-color: #fff;
		border-radius: 2px;
		margin-top: -70px;
		border: 1px solid #ccc
		/* margin-top: -70px */
	}
	.home-func li{
		width: 256px;
		height: 66px;
		display: inline-block;
		margin: 20px 32px 20px 0;
		cursor: pointer;
		position: relative;
	}
	.home-func li>img{
		height: 100%;
		vertical-align: middle
	}
	.home-func li>div{
		display: inline-block;
		vertical-align: middle;
		margin-left: 20px;
	}
	
	.home-func li>div h5{
		font-size: 20px;
		color: #111;
		font-weight: 700
	}
	.home-func li>div p{
		margin-top: 7px;
		color: #999;
		font-size: 14px
	}
	.home-func-mask{
		position: absolute;
		width: 100%;
		height: 100%;
		left: 0;
		top: 0;
		/* background: #666; */
	}
</style>