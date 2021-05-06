<template>
	<div class="home-banner" :class="{bacImg:!isType}">
		<slot></slot>
	</div>
</template>

<script>
export default {
	props:{
		isType:{
			type:Boolean,
			default:false
		},
		isType2:{
			type:Boolean,
			default:false
		}
	}
}
</script>
<style scoped>
	.home-banner{
		/* height: 570px; */
		background: url('../../../assets/image/banner-1x.png') no-repeat;
		background-size:100%
	}
	.bacImg{
		background: url('../../../assets/image/banner-2x.png') no-repeat;
		background-size:100%
	}
</style>