### Project-Bootstrop-wjs
基于Bootstrop响应式开发的项目， 适配多种终端。</br>
包含的Bootstrop相关内容：</br>
响应式开发</br>

栅格系统</br>

javascript组件</br>

固定浮动导航：Affix</br>

	@media screen and (max-width: 768px){
  	.wjs_nav .navbar-collapse{
  	  position:absolute;  
  	  width:100%;
  	  background: #fff;
  	}
	}

ajax异步 动态请求后台轮播图数据。</br>

	function banner() {
    		var getData=function(callback){
       		$.ajax({
          	 url:'json/index.json',
          	 data:{},
           	type:'get',
          	 dataType:'json',
          	 success:function(data){
                	callback && callback(data);
            	}
        	});
    	}
移动端手势滑动：</br>

	var startX=0；
	var moveX=0；
	var distanceX=0；
	var isMove=false；
	$(‘.wjs_banner’).on( ‘ touchstart’ ,  function (e) { 
		startX = e.originalEvent.touches[0].clientX;
	});
	$(‘.wjs_banner’).on( ‘ touchmove’ ,  function (e) {
		moveX = e.originalEvent.touches[0].clientX;
		distanceX= moveX- startX;  
		isMove=true;
	});
	$(‘.wjs_banner’).on( ‘ touchend’ ,  function (e) { 
		if（Math.abs( distancex) > 50 && isMove) {
		if ( distanceX  < 0）{
			//向左滑动  下一张
			$('.carousel').carousel(“next”);
		}else{
       	 		//向右滑动  上一张
			$('.carousel').carousel(“prev”)
		}
	}
	//重置
	startX=0；
	moveX=0；
	distanceX=0；
	isMove=false；
	});

优化的问题：数据缓存原理</br>
页签移动端响应和滑动</br>
产品盒子响应式</br>
bootstrop定制</br>
字体图标</br>
等等。。


