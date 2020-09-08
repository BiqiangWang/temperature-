<template>
	<div id="article-info-container">
		<div id="article-info">
			<span id="article-num">我的文章:233      </span>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<span id="total-comment">收到评论:0     </span>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<span id="total-praise">收到点赞:0     </span>
		</div>
		
	</div>
</template>

<script>
	export default {
	       
	    }
</script>

<style>
	#article-info-container{
		position: absolute;
		width: 982px;
		height: 91px;
		left: 402px;
		top: 389px;
		
		background: #FFFFFF;
	}
	#article-info{
		position: absolute;
		width: 724px;
		height: 51px;
		left: 17px;
		top: 20px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: 290;
		font-size: 18px;
		line-height: 24px;
		display: flex;
		align-items: center;
		
		color: #000000;
	}
	
</style>
