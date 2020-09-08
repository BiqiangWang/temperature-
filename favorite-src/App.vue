<template>
  <div id="app">
	<top v-on:isMenuShow="isMenuShow=$event;"></top>
	        <div id="page">
				<div id="photo">
					<img src="./assets/banner.png" alt="照片">
				</div>
				<div>
					<favorite></favorite>
				</div>
				<footer id="footer">
					Copyright &copy;2020 Temperature team, All Rights Reserved.<br />
					<span>举报中心       联系我们</span>
				</footer>
			</div>
  </div>
</template>

<script>
import top from './components/top.vue'
import favorite from './components/favorite.vue'

export default {
  name: 'app',
  components: {
	top,
	favorite
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
			height: 3000px;
			
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
		left:500px;
		top:2531px;
		
	}
</style>
