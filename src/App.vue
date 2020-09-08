<template>
  <div id="app">
    <top v-on:isMenuShow="isMenuShow=$event;"></top>
            <div id="page">
				<div id="photo">
					<img src="./assets/banner.png" alt="照片">
				</div>
			</div>
			<!--<div>
				<index></index>
				<ArticleContent></ArticleContent>
			</div>-->
			<UploadArticle></UploadArticle>
			
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import top from './components/top.vue'
import index from './components/index.vue'
import ArticleContent from './components/ArticleContent.vue'
import UploadArticle from './components/UploadArticle.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
	top,
	index,
	ArticleContent,
	UploadArticle
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
		height: 2500px;
				
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
</style>
