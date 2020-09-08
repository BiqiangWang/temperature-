<template>
	   <div class="HowPost">
		   <div id="HowPost-title-box"></div>
		   <span id="HowPost-title">热门文章</span>
		   <div id="list">
			   <span>如何制作博客网站</span>
			   <br />
			   <span>如何写3D游戏</span>
		   </div>
	   </div>
</template>

<script>
	export default {
	       
	    }
</script>

<style scoped>
.HowPost{
	position: absolute;
	width: 302px;
	height: 344px;
	left: 45px;
	top: 667px;
	
	background: #FFFFFF;
	border-radius: 20px;
}
#HowPost-title-box{
	position: absolute;
	width: 120px;
	height: 56px;
	left: 0px;
	top: 0px;
	
	background: #B23535;
	border-radius: 0px 0px 30px 0px;
}
#HowPost-title{
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
