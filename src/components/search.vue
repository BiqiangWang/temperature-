<template>
	<div id="container">
		<div id="box">
			<input id="search-info" type="text" />
		</div>
		<div id="search-button"></div>
	</div>
</template>

<script>
	export default {
	  
	}
</script>

<style scoped>
	#container{
		position: absolute;
		width: 303px;
		height: 54px;
		left: 46px;
		top: 569px;
		
		background: #FFFFFF;
	}
	#box{
		position: absolute;
		width: 256px;
		height: 35px;
		left: 23px;
		top: 9px;
		
		background: #E8E2E2;
		border-radius: 8px;
	}
	#search-info{
		position: absolute;
		width: 88px;
		height: 18px;
		left: 18px;
		top: 9px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 14px;
		line-height: 18px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #767373;
	}
	#search-botton{
		position:absolute;
		position: relative;
		width: 75.08px;
		height: 35px;
		left: 203px;
		top: 9px;
		
		background-image: url('../assets/search.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
</style>
