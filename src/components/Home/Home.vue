<template>
	<div class = "tmpl">
		<!--利用mint-ui中的swipe组件实现轮播图-->
	 	<mt-swipe :auto="2000">
		    <mt-swipe-item v-for="(item,index) in list" :key="index">
		  		<img class="img" :src="item.img" alt="轮播图">
		  	</mt-swipe-item>
		</mt-swipe>
		<!--利用mui中的9宫格实现系统的导航按钮-->
		<div class="mui-content">
		        <ul class="mui-table-view mui-grid-view mui-grid-9">
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <router-link to="/news/newslist">
	                    <span class="mui-icon mui-icon-home"></span>
	                    <div class="mui-media-body">新闻资讯</div>
					</router-link >
                    </li>
		           
		            <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <router-link to="/photo/photolist">
	                    <span class="mui-icon mui-icon-navigate"></span>
	                    <div class="mui-media-body">图片分享</div>
	                    </router-link>
                    </li>
                     <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <router-link to="/goods/goodslist">
	                    <span class="mui-icon mui-icon-gear"></span>
	                    <div class="mui-media-body">商品购买</div>
	                    </router-link>
                    </li>
                     <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <a href="#">

	                    <span class="mui-icon mui-icon-paperplane"></span>
	                    <div class="mui-media-body">留言反馈</div>
	                    </a>
                    </li>
                     <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <a href="#">
	                    <span class="mui-icon  mui-icon-info"></span>
	                    <div class="mui-media-body">视频专区</div>
	                    </a>
                    </li>
                     <li class="mui-table-view-cell mui-media mui-col-xs-4 mui-col-sm-3">
		            <a href="#">
	                    <span class="mui-icon  mui-icon-help"></span>
	                    <div class="mui-media-body">联系我们</div>
	                    </a>
                    </li>
		        </ul> 
		</div>
	</div>

	</div>
</template>

<script>
	export default{
			data(){
				return {
					list:[{
						url:'http://www.baidu.com',
						img:'http://ofv795nmp.bkt.clouddn.com/vuelogobanner1.jpg'
					},{
						url:'http://www.baidu.com',
						img:'http://ofv795nmp.bkt.clouddn.com/vuelogobanner2-1.jpg'
				}]
				
			   // list:[]s
		// 	}
		// },
		// created(){
		// 	this.getlunbo();
		// },
		// methods:{
		// 	getlunbo(){
		// 		var url = 'http://vuecms.ittun.com/api/getlunbo';
		// 		this.$http.get(url).then(res=>{
		// 			//成功则将res.body.message中的数据赋值给this.list属性即可
		// 			this.list = res.body.message;
		// 		},res=>{
		// 			console.log('轮播图获取失败');
		// 		});
			}
		}
	}

</script>	

<style scoped>
	.img{
		width:100%;
		height:100%;
	}
  	.mint-swipe {
    overflow: hidden;
    position: relative;
    height: 250px;
  }
  .mint-swipe-items-wrap {
    position: relative;
    overflow: hidden;
    height: 100%;
    -webkit-transform: translateZ(0);
    transform: translateZ(0)
  }
  .mint-swipe-items-wrap > div {
    position: absolute;
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
    width: 100%;
    height: 100%;
    display: none;
  }
  .mint-swipe-items-wrap > div.is-active {
    display: block;
    -webkit-transform: none;
    transform: none;
  }
  .mint-swipe-indicators {
    position: absolute;
    bottom: 10px;
    left: 50%;
    -webkit-transform: translateX(-50%);
    transform: translateX(-50%);
  }
  .mint-swipe-indicator {
    width: 8px;
    height: 8px;
    display: inline-block;
    border-radius: 100%;
    background: #000;
    opacity: 0.2;
    margin: 0 3px;
  }
  .mint-swipe-indicator.is-active {
    background: #fff;
  }
 



 body{
 background-color:red;
 }
 
  .mui-icon{
  	width:50px;
  	height:50px;
  }
   .mui-icon-home{
  	background-image:url(../../../statics/images/menu10.png);
  	background-repeat:round;
  } 
  .mui-icon-navigate{
  	background-image:url(../../../statics/images/menu10.png);
  	background-repeat:round;
  } 
  .mui-icon-gear{
  	background-image:url(../../../statics/images/menu3.png);
  	background-repeat:round;
  }
   .mui-icon-paperplane{
  	background-image:url(../../../statics/images/menu5.png);
  	background-repeat:round;
  } 
  .mui-icon-info{
  	
  	background-image:url(../../../statics/images/menu6.png);
  	background-repeat:round;
  }
   .mui-icon-help{
  	background-image:url(../../../statics/images/menu9.png);
  	background-repeat:round;
  }
  .mui-icon-home:before,
  .mui-icon-navigate:before,
  .mui-icon-gear:before,
  .mui-icon-paperplane:before,
  .mui-icon-info:before,
  .mui-icon-help:before{
  	content:'';
  }

</style>