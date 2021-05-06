<template>
	<div class="home-banner-content">
		<h1>金山词霸</h1>
		<p>涵盖牛津词典、柯林斯高阶词典等55本词书</p>
		<div class="home-search">
			<ul class="home-search-tab">
				<li @click="changeType" :class="{active:isType}">
					查词
				</li>
				<li @click="changeType" :class="{active:isType2}">
					翻译
				</li>
			</ul>
			<form action="javascript:void(0)">
				<input type="text" :placeholder="placeholder">
				<div>

				</div>
			</form>
		</div>
	</div>
</template>
<script>
export default {
	data() {
		return {
			placeholder: '请输入您要翻译的单词',
			isType: true,
			isType2: false,
		}
	},
	methods:{
		changeType() {
			this.isType = !this.isType
			this.isType2 = !this.isType2
			if(this.isType) {
				this.placeholder = '请输入您要翻译的单词'
			}else{
				this.placeholder = '请输入您要翻译的短语或句子'
			}
			console.log(this.isType);
			console.log(this.isType2);
			const type = {
				type1 : this.isType,
				type2 : this.isType2
			}
			this.$emit('changeType',type)
		}
	}
}
</script>
<style scoped>
	.home-banner-content{
		padding-top: 130px;
		width: 680px;
		margin: 0 auto;
		line-height: 1.3;
		padding-bottom: 130px
	}
	.home-banner-content h1{
		font-weight: 600;
		color: #fff;
		font-size: 60px;
	
	}
	.home-banner-content p{
		font-size: 18px;
		color: #fff;
		margin-top: 6px
	}
	/*搜索状态栏 */
	.home-search{
		margin-top: 50px;
		position: relative;
	}
	.home-search-tab li.active{
		color: #333;
		z-index: 2;
		font-weight: 700;
	}
	.home-search-tab li{
		width: 76px;
		height: 38px;
		display: inline-block;
		text-align: center;
		font-size: 20px;
		line-height: 38px;
		color: hsla(0,0%,100%,.4);
		position: relative;
		z-index: 1;
		margin-right: 7px;
		cursor: pointer;
	}
	.home-search-tab li:after{
		/* content: '';
		position: absolute;
		width: 100%;
		top: 0;
		height: 0;
		right: 0;
		left: 0;
		z-index: -1;
		-webkit-transform: perspective(10px) rotateX(4deg) scale(1.35); */
		content: "";
		position: absolute;
		width: 86%;
		height: 100%;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		z-index: -1;
		background-color: rgba(0,0,0,.2);
		-webkit-transform: perspective(10px) rotateX(4deg) scale(1.35);
		transform: perspective(10px) rotateX(4deg) scale(1.35);
		-webkit-transform-origin: bottom left;
		transform-origin: bottom left;
		border-radius: 3px 6px 0 0;
	}
	.home-search-tab li.active:after{
		background: #fff;
	}
	.home-search>form{
		margin-top: -3px;
		margin-left: -1px;
		overflow: hidden;
		border-radius: 0 2px 2px 2px
	}
	.home-search>form input{
		width: 606px;
		height: 56px;
		background: #fff;
		font-size: 16px;
		padding: 20px 22px;
		box-sizing: border-box;
		color: #222
	}
	::-webkit-input-placeholder {
		/* WebKit browsers */
		color: #c5c5c5;
	}

	:-moz-placeholder {
		/* Mozilla Firefox 4 to 18 */
		color: #c5c5c5;
	}

	::-moz-placeholder {
		/* Mozilla Firefox 19+ */
		color: #c5c5c5;
	}

	:-ms-input-placeholder {
		/* Internet Explorer 10+ */
		color: #c5c5c5;
	}
	/*搜索框 */
	.home-search>form div{
		/* width: 74px;
		height: 56px;
		background: url('../../../assets/image/search.png') no-repeat;
		background-size: 50% 50%;
		display: inline-block;
		vertical-align: bottom;
		cursor: pointer;
		background-position: 50%;
		background: #111; */
		width: 74px;
		height: 56px;
		display: inline-block;
		vertical-align: bottom;
		background: url('../../../assets/image/search.png') no-repeat;
		background-size: 30px 30px;
		background-position: 50%;
		background-color: #111;
		cursor: pointer;
		z-index: 2

	}
</style>