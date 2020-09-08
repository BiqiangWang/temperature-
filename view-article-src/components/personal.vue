<template>
  <div class="personal">
	    <div>
			<div id="photo"></div>
		</div>
		<div>
			<div id="name">TEMP</div>
			<div id='sign'>心如止水</div>
		</div>
		<div>
			<button id="focus">
				<span>+关注</span>
			</button>
			<button id="prv-let">
				<span>私信</span>
			</button>
			<button id="per-cen">
				<span>个人中心</span>
			</button>
			
		</div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped>
    .personal{
		position: absolute;
		width: 303px;
		height: 154px;
		left: 46px;
		margin-top: 21px;
		background-color: #ffffff;
	}
	#photo{
		position:absolute;
		position: relative;
		width: 45px;
		height: 45px;
		left: 22px;
		top: 26px;
		
		background-image: url('../assets/search.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	#name{
		position: absolute;
		width: 148px;
		height: 20px;
		left: 98px;
		top: 19px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 14px;
		line-height: 18px;
		display: flex;
		align-items: center;
		letter-spacing: 0.75px;
		text-transform: uppercase;
		
		color: #000000;

	}
	#sign{
		position: absolute;
		width: 151px;
		height: 20px;
		left: 98px;
		top: 47px;
		
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
	#focus{
		position: absolute;
		width: 75px;
		height: 24px;
		left: 16px;
		top: 103px;
		background-color: #FF0000;
		color: #ffffff;
	}
	#prv-let{
		position: absolute;
		width: 76px;
		height: 24px;
		left: 106px;
		top: 103px;
		background-color: #aaaa7f;
		color: #550000;
	}
	#per-cen{
		position: absolute;
		width: 76px;
		height: 24px;
		left: 202px;
		top: 103px;
		background-color: #aaaa7f;
		color: #550000;
	}
</style>
