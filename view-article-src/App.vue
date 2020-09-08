<template>
  <div id="app">
	<top v-on:isMenuShow="isMenuShow=$event;"></top>
	        <div id="page">
				<div>
					<!--<personal></personal>
					<catalog></catalog>
					<HotPosts></HotPosts>
					<comment></comment>
					<test></test>-->
					<ViewArticle></ViewArticle>
				</div>
				<footer id="footer">
					Copyright &copy;2020 Temperature team, All Rights Reserved.<br />
					<span>举报中心       联系我们</span>
				</footer>
			</div>
  </div>
</template>

<script>
import personal from './components/personal.vue'
import top from './components/top.vue'
import catalog from './components/catalog.vue'
import HotPosts from './components/HotPosts.vue'
import comment from './components/comment.vue'
import test from './components/test.vue'
import ViewArticle from './components/ViewArticle.vue'

export default {
  name: 'app',
  components: {
    personal,
	top,
	catalog,
	HotPosts,
	comment,
	test,
	ViewArticle
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
			height: 1500px;
			
			font-family: Microsoft YaHei;
			
			background: #E5E5E5;
}
#r-aside{
		display: inline-block;
		vertical-align: top;
		width: 363px;
		
		margin-left: 57px;
		margin-top: 17px;
		
	}
	#ask-question{
		width: 100%;
		height: 51px;
		
		background: #B23535;
		border-radius: 15px;
		
		font-size: 20px;
		line-height: 51px;
		text-align: center;
		
		color: #FFFFFF;
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
		top:1300px;
	}
</style>
