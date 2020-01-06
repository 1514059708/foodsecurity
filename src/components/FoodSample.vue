<template>
  <div id="control">


    <div id="map">
    </div>

      <!-- 插件导航 -->
    <v-nav></v-nav>
      <!-- Navigation 页面右上角导航页 -->
    <nav class="navbar navbar-default navbar-shrink bounceInDown">
        <div class="container">
            <!-- Brand and toggle get grouped for better mobile display -->
            <div class="navbar-header page-scroll">
                <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1">
                    <span class="sr-only">Toggle navigation</span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
            </div>
    		
            <!-- 菜单栏 -->
            <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
    		
				<form class="form-inline my-2 my-lg-0 ty-search">
					<h1>
						<a href="./">食品安全</a>
					</h1>
					<label for="search-food">
						<i class="fa fa-search" aria-hidden="true"></i>
						<input class="search-input" type="search" placeholder="请输入食品名称" autocomplete="off">
					</label>
					<ul class="search-list">
					</ul>
				    <a class="search-btn"><i class="fa fa-location-arrow" aria-hidden="true"></i></a>
				</form>
            </div>
            <!-- /.navbar-collapse -->
        </div>
        <!-- /.container-fluid -->
    </nav>

    <!-- 左侧弹出框监察重页面：重点食物/重点区域/重点公司 -->
	<div id="sidebar">
	    <div id="jc-wrap">
	        <div id="jcfood" class="sidebar-item">
	            <div>重点食品</div>
			</div>
	        <div id="jccompany" class="sidebar-item">
	            <div>重点企业</div>
			</div>
	        <div id="jcarea" class="sidebar-item">
	            <div>重点区域</div>
	        </div>
	    </div>
	    <!--   侧边关闭按钮，可能不需要
		<div id="closeBar">
	        <span class="glyphicon glyphicon-remove"></span>
	    </div>  -->
	</div>
	<div id="jcfood-content" class="nav-content">
	    <div class="nav-con-close">
	        <i class="glyphicon glyphicon-chevron-left"></i>
	    </div>
	    <div>
	        食品详情
	    </div>
	</div>
	<div id="jccompany-content" class="nav-content">
	    <div class="nav-con-close">
	        <i class="glyphicon glyphicon-chevron-left"></i>
	    </div>
	    <div>
	        company详情
	    </div>
	</div>
	<div id="jcarea-content" class="nav-content">
	    <div class="nav-con-close">
	        <i class="glyphicon glyphicon-chevron-left"></i>
	    </div>
	    <div>
	        quyu详情
	    </div>
	</div>
	
	
	<!-- 右侧关联信息展开栏  -->
	<div id="com-content">
		<div class="close-icon">
		<span onclick="closeContent()"><i class="fa fa-times fa-lg" aria-hidden="true"></i></span>
		</div>
		<div class="row">
			<ul class="nav nav-tabs right-nav">
			  <li class="nav-item">
				<a class="nav-link active right-item" href="#tab1" data-toggle="tab">舆情分析</a>
			  </li>
			  <li class="nav-item">
				<a class="nav-link right-item" href="#tab2" data-toggle="tab">知识图谱</a>
			  </li>
			  <li class="nav-item">
				<a class="nav-link right-item" href="#tab3" data-toggle="tab">监察分析</a>
			  </li>
			</ul>
			<div class="tab-content">
				<div id="tab1" class="tab-pane active">
					<div class="com-content-title">
						<span class="com-content-place">湖北省</span>
					</div>
					<!-- 舆情分析模块的基础信息，比如地理位置，名称，时间 -->
					<div class="yq-basic-info">
						<div>武汉市,[117,30],2019-12-10</div>
					</div>
					<!-- 走势图 -->
					<div id="yq-linechart" style="width: 100%;height: 100%;"></div>
					<!-- 情感分析图 -->
					<div></div>
					<!-- 话题列表 -->
					<div></div>
				</div>
				<div id="tab2" class="tab-pane">这是zj的详细信息</div>
				<div id="tab3" class="tab-pane">这是jc的详细信息</div>
			</div>
		</div>
		
	</div>
  </div>
</template>

<script src="../../static/js/jquery.js"></script>
<script src="../../static/js/bootstrap.js"></script>
<script src="../../static/js/bootstrap.min.js"></script>
<script src="../../static/js/common.js"></script>
<script src="../../static/js/init.js"></script>
<script src="../../static/js/jqBootstrapValidation.js"></script>
<script src="../../static/js/plugins.js"></script>
<script src="../../static/js/tubular.js"></script>
<script src="../../static/js/contact_me.js"></script>
 <script src='https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-language/v0.10.0/mapbox-gl-language.js'></script>
<script>
import mapboxgl from "mapbox-gl";
import MapboxLanguage from '@mapbox/mapbox-gl-language'
import Nav from '@/components/Nav.vue'
export default {
  name: "control_index",
  components: {
    'v-nav': Nav
  },
  data() {
    return {};
  },
  mounted() {
    this.init();
  },
  methods: {
    // 初始化
    init() {
      mapboxgl.accessToken =
        "pk.eyJ1IjoiY2luZHkwNzkiLCJhIjoiY2p5MW0yM2FmMDNhbzNpcnpoeGVqOXpmYSJ9.zKbdCDdA69t7b3zSWctaRw";
      const map = new mapboxgl.Map({
		  container: 'map', // container id
		  style: 'mapbox://styles/mapbox/streets-v9', // stylesheet location
		  center: [110, 37], // starting position [lng, lat]
		  zoom: 3.4 // starting zoom
	  });
	  
    //   const language = new MapboxLanguage({ defaultLanguage: "zh" });
    // map.addControl(language);
    map.addControl(new MapboxLanguage({
      defaultLanguage: 'zh'
    }));

    map.addControl(new mapboxgl.NavigationControl());

    (function() {
      var NavigateBar = function(elementId) {
        this.eId = elementId||'jc-wrap';
        this.el = document.getElementById(this.eId);
        this.el.addEventListener('click',function(evt) {
            evt.stopPropagation();
        });
        this.state = 'allClosed';//hasOpened
        this.currentOpenedEl = null;

        //使用jquery就更方便使用Delegation 
        var forEach = Array.prototype.forEach;
        var self = this;
        console.log("未开始之前的self.state:"+self.state);
        var navigatorList =  document.querySelectorAll('#' + this.eId + ' > div');
        forEach.call(navigatorList, function(navigator){
          navigator.addEventListener('click',function(evt) {
            var currentEl = document.getElementById(evt.currentTarget.id + '-content');
            var currentA = document.getElementById(evt.currentTarget.id);
            if(self.state === 'allClosed') {
              currentEl.className = 'nav-content';
              //  currentEl.style.top = '0px';
              currentEl.classList.add('move_right');
              console.log("diyici开始之前的evt.currentTarget.id:"+evt.currentTarget.id);
              self.state = 'hasOpened';
              self.currentOpenedEl = currentEl;
            } else {
              self.currentOpenedEl.className = 'nav-content';
            //   self.currentOpenedEl.style.top = '0px';
              self.currentOpenedEl.classList.add('move_left');
              currentEl.className = 'nav-content';
          //    currentEl.style.top = '0px';
              currentEl.classList.add('move_right');
              self.currentOpenedEl = currentEl; 
            } 
          });
        });


        var navConCloseBarList = document.querySelectorAll('.nav-content > div.nav-con-close');
        forEach.call(navConCloseBarList, function(navConCloseBar){
            navConCloseBar.addEventListener('click',function(evt) {
                var currentEl = evt.currentTarget.parentNode;
                
                currentEl.className = 'nav-content';
              //   currentEl.style.top = '0px';
                currentEl.classList.add('move_left');
                self.state = 'allClosed';
                var jcf = document.getElementById('jcfood');
                var jcc = document.getElementById('jccompany');
                var jca = document.getElementById('jcarea');
                jcf.classList.remove('sidebar-item-active');
                jcc.classList.remove('sidebar-item-active');
                jca.classList.remove('sidebar-item-active');
                console.log(self,evt);
            });
        });
      };

      NavigateBar.prototype.close = function() {
          this.currentOpenedEl.className = 'nav-content';
        //   this.currentOpenedEl.style.top = '0px';
          this.currentOpenedEl.classList.add('move_left');
         // var currentA = document.getElementById(self.eId);
        //  currentA.classList.remove('sidebar-item-active');
        console.log("this.currentOpenedEl:"+this.currentOpenedEl);
          this.state = 'allClosed';
      }; 

        var navigateBar = new NavigateBar(); 

/*
        var SideBar = function(elementId) {
            this.eId = elementId||'sidebar';
            this.el = document.getElementById(this.eId);
            this.closeBarEl = document.getElementById('closeBar');
            this.state = 'opened';
            var self = this;
            this.el.addEventListener('click',function(evt) {
                if(evt.target !==  self.el) {
                    self.triggerSwitch(); 
                }
            });
        };

        SideBar.prototype.triggerSwitch = function() {
            if(this.state === 'opened')
                this.close();
            else if(this.state === 'closed')
                this.open();
        };

        SideBar.prototype.close = function() {
            navigateBar.close();
            this.el.style.left = '0';
            this.el.className ='move_left';
            this.closeBarEl.style.left = '0';
            this.closeBarEl.className = 'move_right';
            this.state = 'closed';


        };

        SideBar.prototype.open = function() {
            this.el.style.left = '-120px';
            this.el.className = 'move_right';
            this.closeBarEl.style.left = '160px';
            this.closeBarEl.className = 'move_left';
            this.state = 'opened';
        };
        var sideBar = new SideBar();  */

      })();

      $('.sidebar-item').each(function(index){
          $(this).click(function(){
              $(this).addClass('sidebar-item-active').siblings().removeClass('sidebar-item-active');
          });
      });

      
    }
  },
  computed: {
  }
};
</script>

<style scope>

@import '../../static/css/bootstrap.css';
@import '../../static/css/bootstrap.min.css';
@import '../../static/css/animate.css';
@import '../../static/css/style.css';
@import '../../static/css/jcfx.css'; 
@import '../../static/css/pe-icons.css';
@import '../../static/css/font-awesome-4.1.0/css/font-awesome.min.css';
@import url("https://api.tiles.mapbox.com/mapbox-gl-js/v0.51.0/mapbox-gl.css");

#control {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.mapboxgl-ctrl-group {
    border: none;
    box-shadow: none !important;
    -webkit-box-shadow: none !important;
    background: transparent;
}
.mapboxgl-ctrl-group > button,.mapboxgl-ctrl-group > button:hover,.mapboxgl-ctrl-group > button:focus,.mapboxgl-ctrl-group > button:focus {
    width: 2.5em;
    height: 2.5em;
    margin-top: 0.5em;
    border-radius: 2.5em !important;
    border: none !important;
    background-color: #fff !important;
}
@-webkit-keyframes move_right {
			from {
				opacity: 0;
			}
			to {
				opacity: 1;
				-webkit-transform: translateX(120px);
				transform: translateX(120px);
			}
		}
		
		@keyframes move_right {
			from {
				opacity: 0;
			}
			to {
				opacity: 1;
				-webkit-transform: translateX(120px);
				transform: translateX(120px);
			}
		}
		
		@-webkit-keyframes move_left {
			from {
				opacity: 1;
			}
			to {
				opacity: 0;
				-webkit-transform: translateX(-120px);
				transform: translateX(-120px);
			}
		}
		
		@keyframes move_left {
			from {
				opacity: 1;
			}
			to {
				opacity: 0;
				-webkit-transform: translateX(-120px);
				transform: translateX(-120px);
			}
		}
		.move_right {
			-webkit-animation-name            : move_right;
			animation-name            : move_right;
			-webkit-animation-duration        : 1s;
			animation-duration        : 1s;
			-webkit-animation-iteration-count : 1;
			animation-iteration-count : 1;
			-webkit-animation-fill-mode : forwards;
			animation-fill-mode : forwards;
		}
		
		.move_left {
			-webkit-animation-name            : move_left;
			animation-name            : move_left;
			-webkit-animation-duration        : 1s;
			animation-duration        : 1s;
			-webkit-animation-iteration-count : 1;
			animation-iteration-count : 1;
			-webkit-animation-fill-mode : forwards;
			animation-fill-mode : forwards;
    }
    @-webkit-keyframes move_up {
	from {
		opacity: 0;
	}
	to {
		opacity: 1;
		-webkit-transform: translateY(-250px);
		transform: translateY(-250px);
	}
}

@keyframes move_up {
	from {
		opacity: 0;
	}
	to {
		opacity: 1;
		-webkit-transform: translateY(-250px);
		transform: translateY(-250px);
	}
}

.move_up {
	-webkit-animation-name            : move_up;
	animation-name            : move_up;
	-webkit-animation-duration        : 1s;
	animation-duration        : 1s;
	-webkit-animation-iteration-count : 1;
	animation-iteration-count : 1;
	-webkit-animation-fill-mode : forwards;
	animation-fill-mode : forwards;
}
</style>
