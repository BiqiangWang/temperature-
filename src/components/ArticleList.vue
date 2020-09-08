<template>
	<div id="container">
		<div class="article-container" :style="{top: TMTop, left: MLeft + 'px'}">
			<div id="article-title">领悟生活真谛</div>
			<div id="article-summary">看淡点看开点看远点，才是对自己最好的方式</div>
			<div id="publish-time">2020.8.24</div>
			<img id="comment-logo" src="../assets/logo.png" alt="logo"/>
			<div id="comment-num">23</div>
			<button id="delete">删除</button>
		</div>
		<div class="article-container">
			<div id="article-title">领悟生活真谛</div>
			<div id="article-summary">看淡点看开点看远点，才是对自己最好的方式</div>
			<div id="publish-time">2020.8.24</div>
			<img id="comment-logo" src="../assets/logo.png" alt="logo"/>
			<div id="comment-num">23</div>
			<button id="delete">删除</button>
		</div>
	</div>
</template>

<script>
	export default {
	       
	    }
</script>

<style>
	#container{
		position: absolute;
		width: 982px;
		height: 400px;
		left: 402px;
		top: 485px;
		
		border: 1px solid #C4C4C4;
		box-sizing: border-box;
	}
	.article-container{
		display: block;
		width: calc(100% - 10px);
		height: 130px;
		
		margin: 4px 5px;
		
		text-align: center;
		line-height: 54px;
		font-size: 18px;
		color: #FFFFFF;
		background: rgba(255, 255, 127, 0.8);
		border-radius: 6px;
		
		background: rgba(255, 255, 127, 0.8);
		
		cursor: pointer;
	}
	#article-title{
		position: absolute;
		width: 144px;
		height: 93px;
		left: 10px;
		top: 5px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 32px;
		/* identical to box height */
		
		
		color: #000000;

	}
	#article-summary{
		position: absolute;
		width: 962px;
		height: 50px;
		left: 10px;
		top: 44px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		
		color: #727272;

	}
	#publish-time{
		position: absolute;
		width: 147px;
		height: 24px;
		left: 10px;
		top: 101px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		/* identical to box height */
		
		
		color: #000000;
	}
	#comment-logo{
		position: absolute;
		width: 20px;
		height: 20px;
		left: 193px;
		top: 105px;
		
		background: #727272;
	}
	#comment-num{
		position: absolute;
		width: 22px;
		height: 24px;
		left: 225px;
		top: 101px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		/* identical to box height */
		
		
		color: #000000;
	}
	#delete{
		position: absolute;
		width: 60px;
		height: 30px;
		left: 285px;
		top: 101px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		/* identical to box height */
		
		text-decoration-line: underline;
		
		color: #999494;

	}
</style>
