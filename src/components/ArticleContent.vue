<template>
	<div id="container">
		<div id="article-title-container">
			<input id="article-title" type="text" />
		</div>
		<div id="head-container">
			<span id="head">文本编辑器</span>
		</div>
		<div>
			<input id="article-content" />
		</div>
		<div>
			<span id="tag">添加tag:</span>
			<span id="add-tar" @click="AddTarget"></span>
					<div id="tar-menu" v-if="isMenuShow">
						<div id="t-m-learn" class="m-button" :style="{top: TMTop, left: MLeft + 'px'}">学习</div>
						<div id="t-m-life" class="m-button">生活</div>
						<div id="t-m-development" class="m-button">开发</div>
						<div id="t-m-game" class="m-button">游戏</div>
						<div id="t-m-entertainment" class="m-button">娱乐</div>
						<div id="t-m-sports" class="m-button">体育</div>
						<div id="t-m-video" class="m-button">影视</div>
						<div id="t-m-real-time-info" class="m-button">资讯</div>
						<div id="t-m-fashion" class="m-button">时尚</div>
						<div id="t-m-dance" class="m-button">舞蹈</div>
						<div id="t-m-music" class="m-button">音乐</div>
						<div id="t-m-else" class="m-button">其他</div>
					</div>
			<span id="limit">选择权限:</span>
			<span id="add-limit" @click="AddLimit"></span>
					<div id="lim-menu" v-if="isLimMenuShow">
						<div id="l-m-myself" class="l-m-button" :style="{top: TMTop, left: MLeft + 'px'}">仅自己</div>
						<div id="l-m-public" class="l-m-button">公开</div>
					</div>
		</div>
		<div>
			<button id="publish">
				<span id="publish-index">发表</span>
			</button>
			<button id="quit">
				<span id="quit-index">取消</span>
			</button>
		</div>
	</div>
</template>

<script>
	export default{
		name:"ArticleContent",
		methods:{
			AddTarget(){
				this.isMenuShow = this.isMenuShow == false?true:false;
			},
			AddLimit(){
				this.isLimMenuShow = this.isLimMenuShow ==false?true:false;
			}
		},
		data(){
			return {
				isMenuShow: false,
				isLimMenuShow: false,
			};
		}
	}
</script>

<style>
	#container{
		position: absolute;
		width: 1345px;
		height: 1889px;
		left: 48px;
		top: 506px;
		
		background: #FFFFFF;
	}
	#article-title-container{
		position: absolute;
		width: 1194px;
		height: 79px;
		left: 59px;
		top: 85px;
		
		background: #FFFFFF;
		border: 1px solid #000000;
		box-sizing: border-box;
		box-shadow: inset 0px 2px 4px rgba(0, 0, 0, 0.25);
	}
	#article-title{
		position: absolute;
		width: 236px;
		height: 38px;
		left: 20px;
		top: 24px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		
		color: #9F9E9E;

	}
	#head-container{
		position: absolute;
		width: 1194px;
		height: 151px;
		left: 59px;
		top: 187px;
		
		background: #C4C4C4;
	}
	#head{
		position: absolute;
		width: 355px;
		height: 67px;
		left: 60px;
		top: 44px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		
		color: #000000;

	}
	#article-content{
		position: absolute;
		width: 1194px;
		height: 584px;
		left: 59px;
		top: 338px;
		
		background: #FFFFFF;
		border: 1px solid #847E7E;
		box-sizing: border-box;
	}
	#tag{
		position: absolute;
		width: 177px;
		height: 40px;
		left: 68px;
		top: 962px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		
		color: #000000;
	}
	#limit{
		position: absolute;
		width: 169px;
		height: 35px;
		left: 503px;
		top: 967px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 32px;
		display: flex;
		align-items: center;
		
		color: #000000;
	}
	#add-tar{
		position:absolute;
		width: 170px;
		height: 38px;
		left: 173px;
		top: 964px;
		
		background: rgba(255, 255, 127, 0.6);
		
		cursor: pointer;
	}
	#tar-menu{
		position: absolute;
		width: 170px;
		height: 632px;
		left: 173px;
		top: 1018px;
		
		background: #FFFFFF;
		border: 1px solid #C4C4C4;
		box-sizing: border-box;
	}
	.m-button{
			display: block;
			width: calc(100% - 10px);
			height: 54px;
			
			margin: 4px 5px;
			
			text-align: center;
			line-height: 54px;
			font-size: 18px;
			color: #FFFFFF;
			background: rgba(48, 46, 46, 0.77);
			border-radius: 6px;
			
			background: rgba(48, 46, 46, 0.77);
			
			cursor: pointer;
		}	
	#add-limit{
		position:absolute;
		width: 170px;
		height: 38px;
		left: 633px;
		top: 964px;
		
		background: rgba(255, 255, 127, 0.6);
		
		cursor: pointer;
	}
	#lim-menu{
		position: absolute;
		width: 170px;
		height: 632px;
		left: 633px;
		top: 1018px;
		
		background: #FFFFFF;
		border: 1px solid #C4C4C4;
		box-sizing: border-box;
	}
	.l-m-button{
		display: block;
		width: calc(100% - 10px);
		height: 54px;
		
		margin: 4px 5px;
		
		text-align: center;
		line-height: 54px;
		font-size: 18px;
		color: #FFFFFF;
		background: rgba(48, 46, 46, 0.77);
		border-radius: 6px;
		
		background: rgba(48, 46, 46, 0.77);
		
		cursor: pointer;
	}
	#publish{
		position: absolute;
		width: 159px;
		height: 42px;
		left: 902px;
		top: 1096px;
		
		background: #DA4646;
		box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
		border-radius: 4px;
	}
	#publish-index{
		position: absolute;
		width: 103px;
		height: 20px;
		left: 28px;
		top: 13px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		display: flex;
		align-items: center;
		
		color: #F9F5F5;
	}
	#quit{
		position: absolute;
		width: 159px;
		height: 42px;
		left: 1119px;
		top: 1096px;
		
		background: #EFE7E7;
		box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
		border-radius: 4px;
	}
	#quit-index{
		position: absolute;
		width: 103px;
		height: 20px;
		left: 28px;
		top: 13px;
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		font-size: 18px;
		line-height: 24px;
		display: flex;
		align-items: center;
		text-align: center;
		
		color: #504C4C;

	}
</style>
