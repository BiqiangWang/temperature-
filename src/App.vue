<template>
  <div id="app">
    <top v-on:isMenuShow="isMenuShow=$event;"></top>
            <div id="page">
				<div id="photo">
					<img src="./assets/banner.png" alt="照片">
				</div>
				<!--<div>
					<personal></personal>
					<search></search>
					<HottestArticle></HottestArticle>
					<LatestComment></LatestComment>
				</div>
				<div>
					<ArticleInfo></ArticleInfo>
					<ArticleList></ArticleList>
				</div>-->
				<MyArticle></MyArticle>
			</div>
		
			<footer id="footer">
				Copyright &copy;2020 Temperature team, All Rights Reserved.<br />
				<span>举报中心       联系我们</span>
			</footer>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import top from './components/top.vue'
import personal from './components/personal.vue'
import search from './components/search.vue'
import HottestArticle from './components/HottestArticle.vue'
import LatestComment from './components/LatestComment.vue'
import ArticleInfo from './components/ArticleInfo.vue'
import ArticleList from './components/ArticleList.vue'
import MyArticle from './components/MyArticle.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
	top,
	personal,
	search,
	HottestArticle,
	LatestComment,
	ArticleInfo,
	ArticleList,
	MyArticle
  }
}
</script>

<style>
	#app {
	  font-family: 'Avenir', Helvetica, Arial, sans-serif;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	  text-align: center;
	  color: #2c3e50;
	  margin-top: 60px;
	}
	#page{
		width: 100%;
		height: 2800px;
				
		font-family: Microsoft YaHei;
				
		background: #E5E5E5;
	}
    #photo{
		width: calc(100% - 0px);
		height: 312px;
		overflow: hidden;
	}
	#photo>img{
		width: 100%;
		margin-top: calc((0px - 600px + 352px) / 2 + 40px) ;	/*更换图片需要注意修改*/
	}
	footer{
		left:0px;
		top:1000px;
		
		padding: 100px 0px;
		font-size: 18px;
		line-height: 25px;
		text-align: center;
		
		color: #999494;
	}
	#footer{
		position: absolute;
		left:600px;
		top:2600px;
	}
</style>
