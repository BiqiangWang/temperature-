<template>
	   <div class="LatestComment">
		   <div id="LatestComment-title-box"></div>
		   <span id="LatestComment-title">最新评论</span>
		   <div id="list">
			   <span>平安是福:你太有才了！</span>
			   <br />
			   <span>云淡风轻:给你点赞！！</span>
		   </div>
	   </div>
</template>

<script>
	export default {
	       
	    }
</script>

<style scoped>
.LatestComment{
	position: absolute;
	width: 302px;
	height: 344px;
	left: 45px;
	top: 1067px;
	
	background: #FFFFFF;
	border-radius: 20px;
}
#LatestComment-title-box{
	position: absolute;
	width: 120px;
	height: 56px;
	left: 0px;
	top: 0px;
	
	background: #B23535;
	border-radius: 0px 0px 30px 0px;
}
#LatestComment-title{
	position: absolute;
	width: 230px;
	height: 37px;
	left: 22px;
	top: 10px;
	
	font-family: Microsoft YaHei;
	font-style: normal;
	font-weight: bold;
	font-size: 18px;
	line-height: 24px;
	display: flex;
	align-items: center;
	letter-spacing: 0.75px;
	text-transform: uppercase;
	
	color: #FFFFFF;
}
#list{
	position: absolute;
	width: 264.63px;
	height: 247px;
	left: -30px;
	top: 81px;
	
	font-family: Microsoft YaHei;
	font-style: normal;
	font-weight: normal;
	font-size: 14px;
	line-height: 18px;
	letter-spacing: 0.75px;
	text-transform: uppercase;
	
	color: #363535;
}
</style>
