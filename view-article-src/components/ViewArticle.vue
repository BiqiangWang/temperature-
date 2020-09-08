<template>
	<div>
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
		<div class="catalog">
				   <div id="catalog-title-box"></div>
				   <span id="catalog-title">目录</span>
				   <div id="list">
					   <!--<span>1.如何制作博客网站</span>
					   <br />
					   <span>2.如何写一个D游戏</span>-->
					   <div class="left-aside-list-item" v-for="item in Catalog">
					     {{item.title}}
					   </div>
				   </div>
		</div>
		<div class="HowPost">
				   <div id="HowPost-title-box"></div>
				   <span id="HowPost-title">热门文章</span>
				   <div id="list">
					   <!--<span>如何制作博客网站</span>
					   <br />
					   <span>如何写3D游戏</span>-->
					   <div class="left-aside-list-item" v-for="item in HArticles">
					     {{item.title}}
					   </div>
				   </div>
		</div>
		<div id="content-container">
			<div id="content-title">
				<span>如何快速写出一个博客网站</span>
			</div>
			<div id="content-data">
				<div id="time-logo"></div>
				&nbsp;&nbsp;&nbsp;
				<span>2020.8.24</span>
				&nbsp;&nbsp;&nbsp;&nbsp;
				<div id="praise-logo"></div>
				&nbsp;&nbsp;&nbsp;
				<span>233</span>
				&nbsp;&nbsp;&nbsp;&nbsp;
				<div id="collect-logo1"></div>
				&nbsp;&nbsp;&nbsp;
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
		<div class="comment-container">
			<!--<img id="person-logo" src="../assets/logo.png" alt="logo"/>-->
			<div id="comment-edit">
				<div class="person-logo"></div>
				<input id="comment-container" />
				<button id="add-comment" @click="addComment()">添加评论</button>
			</div>
			<div id="comment-list">
				<div class="person-logo"></div>
				<div class="comment-text">
					<span class ="test">TEMP:很美的文字，谢谢分享！</span>
				</div>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<img class="praise-logo" src='../assets/hand.png' alt='logo'/>
				<div class="praise-num">{{praisenum}}</div>
			</div>
			<div id="comment-list2">
				<div class="person-logo"></div>
				<div class="comment-text">
					<span class ="test">TEMP:很美的文字，谢谢分享！</span>
				</div>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<img class="praise-logo" src='../assets/hand.png' alt='logo'/>
				<div class="praise-num">{{praisenum}}</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
	       name:"viewArticle",
		   data(){
		   	return {
				praisenum:2333,
		   		Catalog:[
		   		  {
		   		    topicID: 1,
		   		    title: "1.如何制作博客网站"
		   		  },
		   		  {
		   		    topicID: 2,
		   		    title: "2.如何写一个D游戏"
		   		  }
		   		],
		   		HArticles:[
		   		  {
		   		    topicID: 1,
		   		    title: "如何制作博客网站"
		   		  },
		   		  {
		   		    topicID: 2,
		   		    title: "如何写3D游戏"
		   		  }
		   		],
		   	};
		   },
		   /*created:function(){
		   	  this.addComment();
		   },*/
	       methods:{
	       	addComment(){
				var Nickname = "www";
				var title = "title";
				var content ="whywhywhywhy";
				var headerToken="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJ3d3ciLCJqdGkiOiJkZmIyOTkxMS1iODgzLTQ1ZDAtYjQyNy1lMjhhYWRkMjhlZjEiLCJleHAiOjE1OTk1NzkyMjQsImlzcyI6Imh0dHBzOi8vd3d3LmNuYmxvZ3MuY29tL2NoZW5ndGlhbiIsImF1ZCI6Imh0dHBzOi8vd3d3LmNuYmxvZ3MuY29tL2NoZW5ndGlhbiJ9.AnV2TGhNDPWlmea5sXgMjyH0EV-gmi3Plzw3DLCo_3k";
				this.ajax = new XMLHttpRequest();
				this.ajax.open("POST", "http://139.224.255.43:7779/Article/createArticleCommentByNickName?nick_name="+Nickname+"&title="+title+"&content="+content, true);
				this.ajax.setRequestHeader('Authorization','Bearer '+headerToken);
				this.ajax.onreadystatechange = this.ACsuccessfully;
				this.ajax.send();
			},
			ACsuccessfully(){
				if (this.ajax.readyState == 4 && this.ajax.status == 200) {
				  var receive = this.ajax.responseText;
				  document.getElementById("add-comment").innerHTML=receive;
				  /*for(var i = 0; i < this.LTopics.length; i++){
				    this.LTopics[i].TopicUploadTime=this.LTopics[i].TopicUploadTime.replace("T","  ");
				  }*/
				}
			}
	       },
	       
	    }
</script>

<style>
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
		
		background-image: url('../assets/head1.jpg');
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
		border: none;
	}
	#prv-let{
		position: absolute;
		width: 76px;
		height: 24px;
		left: 106px;
		top: 103px;
		background-color: #aaaa7f;
		color: #550000;
		border: none;
	}
	#per-cen{
		position: absolute;
		width: 76px;
		height: 24px;
		left: 202px;
		top: 103px;
		background-color: #aaaa7f;
		color: #550000;
		border: none;
	}
	
	
	.catalog{
		position: absolute;
		width: 302px;
		height: 375px;
		left: 45px;
		top: 267px;
		
		background: #FFFFFF;
		border-radius: 20px;
	}
	#catalog-title-box{
		position: absolute;
		width: 120px;
		height: 56px;
		left: 0px;
		top: 0px;
		
		background: #B23535;
		border-radius: 0px 0px 30px 0px;
	}
	#catalog-title{
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
	.left-aside-list-item{
		padding: 10px 10px;
		
		/*实现超过一行的显示省略号*/
		white-space: nowrap;
		text-overflow: ellipsis;
		overflow: hidden;
	}
	
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
	#content-data{
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
	#time-logo{
		position:absolute;
		width: 20px;
		height: 20px;
		left: 0px;
		top: 10px;
		
		background-image: url('../assets/timelogo.jpg');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	#praise-logo{
		position:absolute;
		width: 20px;
		height: 20px;
		left: 180px;
		top: 10px;
		
		background-image: url('../assets/hand.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	#collect-logo1{
		position:absolute;
		width: 20px;
		height: 20px;
		left: 280px;
		top: 10px;
		
		background-image: url('../assets/star.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	#target-logo{
		position: absolute;
		width: 20px;
		height: 20px;
		left: 39px;
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
		width: 15px;
		height: 15px;
		left: 29px;
		top: 12px;
		
		/* Gray 5 */
		
		background: #E0E0E0;
		
		background-image: url('../assets/hand.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
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
		width: 15px;
		height: 15px;
		left: 200px;
		top: 12px;
		
		/* Gray 5 */
		background-image: url('../assets/star.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
		
	
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
	.person-logo{
		position:absolute;
		position: relative;
		width: 45px;
		height: 45px;
		left: 22px;
		top: 26px;
		
		background-image: url('../assets/head1.jpg');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	.comment-text{
		position: absolute;
		width: 897px;
		height: 36px;
		left: 88px;
		top: 29px;
		
		background: #FFFFFF;
	}
	.test{
		position: absolute;
		left:0px;
		top: 10px;
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
		left:892px;
		top: 42px;
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
	}
</style>
