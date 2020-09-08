<template>
	<div class="comment-container">
		<!--<img id="person-logo" src="../assets/logo.png" alt="logo"/>-->
		<div id="comment-edit">
			<div class="person-logo"></div>
			<input id="comment-container" />
			<button id="add-comment">添加评论</button>
		</div>
		<div id="comment-list">
			<div class="person-logo"></div>
			<div class="comment-text">TEMP:很美的文字，谢谢分享！</div>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<img class="praise-logo" src='../assets/logo.png' alt='logo'/>
			<div class="praise-num">233</div>
		</div>
		<div id="comment-list2">
			<div class="person-logo"></div>
			<div class="comment-text">TEMP:很美的文字，谢谢分享！</div>
			&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
			<img class="praise-logo" src='../assets/logo.png' alt='logo'/>
			<div class="praise-num">233</div>
		</div>
	</div>
</template>

<script>
	export default {
	       
	    }
</script>

<style>
	.comment-container{
		position: absolute;
		width: 1010px;
		height: 476px;
		left: 382px;
		top: 668px;
		
		background: #FFFFFF;
	}
	#comment-edit{
		position: absolute;
		width: 1010px;
		height: 70px;
		left: 0px;
		top: 0px;
		
		background: #FFFFFF;
	}
	.person-logo{
		position: absolute;
		width: 28px;
		height: 34px;
		left: 32px;
		top: 24px;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 34px 34px 0px;
		
		background: url('../assets/search.png');
	}
	#comment-container{
		position: absolute;
		width: 751px;
		height: 45px;
		left: 85px;
		top: 19px;
		
		background: #F7F7F7;
		border: 1px solid #8B8888;
		box-sizing: border-box;
	}
	#add-comment{
		position: absolute;
		width: 138px;
		height: 45px;
		left: 852px;
		top: 19px;
		
		color: #FFFFFF;
		background: #B23535;
		border-radius: 4px;

	}
	#comment-list{
		position: absolute;
		width: 1010px;
		height: 73px;
		left: 0px;
		top: 75px;
		
		background: #FFFFFF;
	}
	#comment-list2{
		position: absolute;
		width: 1010px;
		height: 73px;
		left: 0px;
		top: 150px;
	}
	.comment-text{
		position: absolute;
		width: 897px;
		height: 36px;
		left: 88px;
		top: 29px;
		
		background: #FFFFFF;
	}
	.praise-logo{
		position: absolute;
		width: 28px;
		height: 34px;
		left:852px;
		top: 33px;
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
	}
	.praise-num{
		position: absolute;
		width: 28px;
		height: 34px;
		left:882px;
		top: 33px;
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
	}
</style>
