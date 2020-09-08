<template>
	<div id="content-container">
		<div id="content-title">
			<span>如何快速写出一个博客网站</span>
		</div>
		<div id="contnt-data">
			<span>2020.8.24</span>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<span>233</span>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<span> 23333</span>
		</div>
		<div>
			<div id="target-logo"></div>
			<div id="target">
				<span>tag:开发</span>
			</div>
		</div>
		<div id="bottom">
			<div id="agree-logo"></div>
			<div id="agree">
				<span>赞同该作者</span>
			</div>
			<div id="collect-logo"></div>
			<div id="collect">
				<span>收藏</span>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
	       
	    }
</script>

<style scoped>
	#content-container{
		position: absolute;
		width: 1010px;
		height: 561px;
		left: 382px;
		top: 80px;
		
		background: #ffffff;
	}
	#content-title{
		position: absolute;
		width: 471px;
		height: 46px;
		left: 26px;
		top: 26px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #000000;
	}
	#contnt-data{
		position: absolute;
		width: 925px;
		height: 39px;
		left: 41px;
		top: 66px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #000000;
	}
	#target-logo{
		position: absolute;
		width: 12px;
		height: 12px;
		left: 49px;
		top: 112px;
		
		/* Icons Color */
		
		background: #78909C;
		
		background-image: url('../assets/search.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 12px 12px 0px;
	}
	#target{
		position: absolute;
		width: 281px;
		height: 20px;
		left: 64px;
		top: 110px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 13px;
		line-height: 17px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: lowercase;
		
		color: #6A6969;
	}
	#bottom{
		position: absolute;
		width: 1010px;
		height: 37px;
		left: 0px;
		top: 524px;
		
		background: #9B9797;
	}
	#agree-logo{
		position: absolute;
		width: 12px;
		height: 11px;
		left: 31px;
		top: 14px;
		
		/* Gray 5 */
		
		background: #E0E0E0;
		
		background-image: url('../assets/search.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 12px 11px 0px;
	}
	#agree{
		position: absolute;
		width: 104px;
		height: 17px;
		left: 51px;
		top: 11px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: bold;
		font-size: 14px;
		line-height: 18px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #E5E5E5;
	
	}
	#collect-logo{
		position: absolute;
		width: 13px;
		height: 13px;
		left: 200px;
		top: 12px;
		
		/* Gray 5 */
		
		background: #E0E0E0;
	
	}
	#collect{
		position: absolute;
		width: 91px;
		height: 16px;
		left: 221px;
		top: 11px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: bold;
		font-size: 14px;
		line-height: 18px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #E5E5E5;
	
	}
</style>
