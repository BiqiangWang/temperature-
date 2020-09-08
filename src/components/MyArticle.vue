<template>
	<div>
		<div id="personal">
			    <div>
					<div id="head-photo"></div>
				</div>
				<div>
					<div id="name">TEMP</div>
					<div id='sign'>心如止水</div>
				</div>
				<button id="see">查看</button>
				<div id="person-info">
					<span id="focus">关注：{{focusnum}}</span>
					&nbsp;&nbsp;&nbsp;&nbsp;
					<span>|</span>
					&nbsp;&nbsp;&nbsp;&nbsp;
					<span id="fans">粉丝：{{fansnum}}</span>
				</div>
		</div>
		<div id="search-container">
			<div id="search-box">
				<input id="search-info" placeholder="搜索我的文章..." type="text" />
				<div id="search-button"></div>
			</div>
		</div>
		<div class="hottest-article">
				   <div id="article-title-box"></div>
				   <span id="hottest-article-title">最热文章</span>
				   <div id="article-list">
					   <span>1.如何制作博客网站</span>
					   <br />
					   <span>2.如何写一个D游戏</span>
				   </div>
		</div>
		<div class="LatestComment">
				   <div id="LatestComment-title-box"></div>
				   <span id="LatestComment-title">最新评论</span>
				   <div id="comment-list">
					   <span>平安是福:你太有才了！</span>
					   <br />
					   <span>云淡风轻:给你点赞！！</span>
				   </div>
		</div>
		<div id="article-info-container">
			<div id="article-info">
				<span id="article-num">我的文章:{{myarticlenum}}     </span>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<span>|</span>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<span id="total-comment">收到评论:{{receivedcommentnum}}    </span>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<span>|</span>
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<span id="total-praise">收到点赞:{{receivedpraisenum}}    </span>
			</div>
			
		</div>
		<div id="container">
			<div class="article-container" v-for="item in MyArticle" :key="item.ArticleID">
				<div class="article-title">{{item.title}}</div>
				<div class="article-summary">{{item.summary}}</div>
				<div class="publish-date">{{item.date}}</div>
				<div class="publish-time">{{item.time}}</div>
				<img class="comment-logo" src="../assets/评论.jpg" alt="logo"/>
				<div class="comment-num">{{item.commentCount}}</div>
				<span class="delete" @click="DeleteArticle()">删除</span>
				<span id="test1">测试删除返回</span>
			</div>
			<!--<div id="article-container2">
				<div class="article-title">领悟生活真谛</div>
				<div class="article-summary">
					<span class="test">看淡点看开点看远点，才是对自己最好的方式</span>
				</div>
				<div class="publish-time">2020.8.24--20：20</div>
				<img class="comment-logo" src="../assets/评论.jpg" alt="logo"/>
				<div class="comment-num">23</div>
				<button class="delete">删除</button>
			</div>
			<div id="article-container3">
				<div class="article-title">领悟生活真谛</div>
				<div class="article-summary">
					<span class="test">看淡点看开点看远点，才是对自己最好的方式</span>
				</div>
				<div class="publish-time">2020.8.24--20：20</div>
				<img class="comment-logo" src="../assets/评论.jpg" alt="logo"/>
				<div class="comment-num">23</div>
				<button class="delete">删除</button>
			</div>
			<div id="article-container4">
				<div class="article-title">领悟生活真谛</div>
				<div class="article-summary">
					<span class="test">看淡点看开点看远点，才是对自己最好的方式</span>
				</div>
				<div class="publish-time">2020.8.24--20：20</div>
				<img class="comment-logo" src="../assets/评论.jpg" alt="logo"/>
				<div class="comment-num">23</div>
				<button class="delete">删除</button>
			</div>-->
		</div>
		<div id="myarticle-page-controller">
			<div id="m-last-page">上一页</div>
		<div class="m-page-num" v-for="item in pageNums">
		  {{item.page}}
		</div>
			<div id="m-next-page">下一页</div>
		</div>
	</div>
</template>

<script>
	export default {
	       name:'myarticle',
	       data(){
	       	return{
				focusnum:1,
				fansnum:2,
				myarticlenum:233,
				receivedcommentnum:123,
				receivedpraisenum:3456,
	       		MyArticle: [
	       		{
	       			ArticleID: 1,
	       			title: "领悟生活真谛",
	       			summary: "谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的谁说的",
	       			date: "2020-08-22",
	       			time: "22:20",
	       			commentCount: 22
	       		},
	       		{
	       			ArticleID: 2,
	       			title: "领悟生活真谛",
	       			summary: "看淡点看开点看远点，才是对自己最好的方式",
	       			date: "2020-08-22",
	       			time: "22:21",
	       			commentCount: 23
	       		},
				{
					ArticleID: 3,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:22",
					commentCount: 24
				},
				{
					ArticleID: 4,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:23",
					commentCount: 25
				},
				{
					ArticleID: 5,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:24",
					commentCount: 26
				},
				{
					ArticleID: 6,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:24",
					commentCount: 26
				},
				{
					ArticleID: 7,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:24",
					commentCount: 26
				},
				{
					ArticleID: 8,
					title: "领悟生活真谛",
					summary: "看淡点看开点看远点，才是对自己最好的方式",
					date: "2020-08-22",
					time: "22:24",
					commentCount: 26
				},
	       		],
	       				pageNums:[
	       					{page: 1},
	       					{page: 2},
	       					{page: 3}
	       				],
	       				selectedPage: 1,
	       	}
	       },
		   methods:{
			   DeleteArticle(){
				   var Nickname = "www";
				   var title = "title";
				   var headerToken="eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJ3d3ciLCJqdGkiOiJkZmIyOTkxMS1iODgzLTQ1ZDAtYjQyNy1lMjhhYWRkMjhlZjEiLCJleHAiOjE1OTk1NzkyMjQsImlzcyI6Imh0dHBzOi8vd3d3LmNuYmxvZ3MuY29tL2NoZW5ndGlhbiIsImF1ZCI6Imh0dHBzOi8vd3d3LmNuYmxvZ3MuY29tL2NoZW5ndGlhbiJ9.AnV2TGhNDPWlmea5sXgMjyH0EV-gmi3Plzw3DLCo_3k";
				   this.ajax = new XMLHttpRequest();
				   this.ajax.open("POST", "http://139.224.255.43:7779/Article/deleteArticleByTitle?nick_name="+Nickname+"&title="+title, true);
				   this.ajax.setRequestHeader('Authorization','Bearer '+headerToken);
				   this.ajax.onreadystatechange = this.DAsuccessfully;
				   this.ajax.send();
			   },
			   DAsuccessfully(){
				   if (this.ajax.readyState == 4 && this.ajax.status == 200) {
				     var receive = this.ajax.responseText;
				     document.getElementById("test1").innerHTML=receive;
				   }
			   }
		   }
	    }
</script>


<style>
	#personal{
		position: absolute;
		width: 303px;
		height: 154px;
		left: 46px;
		margin-top: 21px;
		background-color: #ffffff;
	}
	#head-photo{
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
	#see{
		position: absolute;
		width: 58px;
		height: 24px;
		left: 206px;
		top: 27px;
		background-color: #FF0000;
		color: #ffffff;
		border: none;
	}
	#see:focus{
		outline:#000000;
	}
	#person-info{
		position: absolute;
		width: 177px;
		height: 20px;
		left: 30px;
		top: 93px;
		
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
	
	
	#search-container{
		position: absolute;
		width: 303px;
		height: 54px;
		left: 46px;
		top: 569px;
		
		background: #FFFFFF;
	}
	#search-box{
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
		width: 188px;
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
		border: none;/*input边框不显示*/
		
		color: #767373;
	}
	#search-info:focus{
		outline: none;
	}
	#search-button{
		position:absolute;
		width: 75.08px;
		height: 35px;
		left: 190px;
		top: 0px;
		
		background-image: url('../assets/search.png');
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		border-radius: 0px 30px 30px 0px;
	}
	
	.hottest-article{
		position: absolute;
		width: 302px;
		height: 375px;
		left: 45px;
		top: 649px;
		
		background: #FFFFFF;
		border-radius: 20px;
	}
	#article-title-box{
		position: absolute;
		width: 120px;
		height: 56px;
		left: 0px;
		top: 0px;
		
		background: #B23535;
		border-radius: 0px 0px 30px 0px;
	}
	#hottest-article-title{
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
	#article-list{
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
	#comment-list{
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
	
	
	#container{
		position: absolute;
		width: 982px;
		height: 1000px;
		left: 402px;
		top: 485px;
		
		border: 1px solid #C4C4C4;
		box-sizing: border-box;
		border: none;
	}
	.article-container{
		width: 935px;
		margin-top: 5px;
		text-align: left;
		padding: 20px;
			
		background: #FFFFFF;
		box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.25);
		cursor: pointer;
	}
	#article-container2{
		position: absolute;
		width: 982px;
		height: 130px;
		left: -5px;
		top: 140px;
		
		margin: 4px 5px;
		line-height: 54px;
		font-size: 18px;
		background: rgba(255, 255, 255, 0.8);
		cursor: pointer;
	}
	#article-container3{
		position: absolute;
		width: 982px;
		height: 130px;
		left: -5px;
		top: 280px;
		
		margin: 4px 5px;
		line-height: 54px;
		font-size: 18px;
		background: rgba(255, 255, 255, 0.8);
		cursor: pointer;
	}
	#article-container4{
		position: absolute;
		width: 982px;
		height: 130px;
		left: -5px;
		top: 420px;
		
		margin: 4px 5px;
		line-height: 54px;
		font-size: 18px;
		background: rgba(255, 255, 255, 0.8);
		cursor: pointer;
	}
	.article-title{
		display: block;
				position: relative;
				font-size: 24px;
				line-height: 24px;
				color: #000000;
			
		/*实现超过一行的显示省略号*/
		white-space: nowrap;
		text-overflow: ellipsis;
		overflow: hidden;
	
	}
	.article-summary{
		margin-top: 10px;
		margin-bottom: 10px;
				height: 50px;
			
				font-size: 18px;
				line-height: 25px;
				color: #727272;
			
		/*实现显示两行文字后显示省略号*/
				display: -webkit-box;
		-webkit-line-clamp: 2;
		-webkit-box-orient: vertical;
		text-overflow: ellipsis;
		overflow: hidden;
	
	}
	.test{
		position: absolute;
		left:5px;
		top: 0px;
	}
	.publish-date{
		display: inline-block;
		width: max-content;
			
		font-size: 18px;
		line-height: 18px;
		color: #000000;
	}
	.publish-time{
		display: inline-block;
		margin-left: 20px;
		width: fit-content;
		font-size: 18px;
		line-height: 18px;
		color: #000000;
	}
	.comment-logo{
		position: absolute;
		width: 20px;
		height: 20px;
		left: 223px;
		top: 122px;
		
		background: #727272;
	}
	.comment-num{
		display: inline-block;
		margin-left: 60px;
		width: fit-content;
			
		font-size: 18px;
		line-height: 18px;
			
		color: #000000;
	}
	.delete{
		display: inline-block;
		margin-left: 60px;
		width: fit-content;
			
		font-size: 18px;
		line-height: 25px;
		text-decoration-line: underline;
			
		
		font-family: Microsoft YaHei;
		font-style: normal;
		font-weight: normal;
		/* identical to box height */
		
		color: #999494;
	
	}
	#test1{
		position: absolute;
		width: 200px;
		height: 30px;
		left: 485px;
		top: 121px;
		color: #999494;
		 z-index:999;
	}
	
	
	#myarticle-page-controller{
		position: absolute;
		width: 982px;
		height: 100px;
		left: 364px;
		top: 1858px;
		
	  display: flex;
	  align-items: center;
		margin-top: 20px;
		font-size: 18px;
	  line-height: 18px;
	}
	#m-last-page{
	  flex-grow: 1;
		margin-right: 60px;
	  text-align: right;
	  cursor: pointer;
	}
	.m-page-num{
	  display: flex;
	  justify-content: center;
	  align-items: center;
		width: 40px;
		height:40px;
		color: #727272;
		border-radius: 5px;
	  cursor: pointer;
	}
	.m-page-num:hover{
	  background: rgba(114, 114, 114, 0.2);
	}
	.m-page-num-selected{
		background: rgba(114, 114, 114, 0.3);
	}
	#m-next-page{
	  flex-grow: 1;
		margin-left: 60px;
	  text-align: left;
	  cursor: pointer;
	}
	
	
	
</style>
