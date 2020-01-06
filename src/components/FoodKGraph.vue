<template>
  <div id="knowledge">

      <!-- 插件导航 -->
    <v-nav></v-nav>
      <!-- Navigation -->
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
	
	<!-- 可收缩列表 
	<div id="mySidebar" class="sidebar" onmouseover="toggleSidebar()" onmouseout="toggleSidebar()"></div> -->
	
    <!-- 左侧弹出框监察重页面：重点食物/重点区域/重点公司 -->
	<div id="zs-sidebar">
	    <div id="zs-wrap">
	        <div id="zsfood" class="zs-sidebar-item">
	            <div>食品风险知识</div>
			</div>
	        <div id="zscompany" class="zs-sidebar-item">
	            <div>相关食品安全</div>
			</div>
	        <div id="zsarea" class="zs-sidebar-item">
	            <div>食品安全监察</div>
	        </div>
	    </div>
	    <!--   侧边关闭按钮，可能不需要
		<div id="closeBar">
	        <span class="glyphicon glyphicon-remove"></span>
	    </div>  -->
	</div>
	<div id="zsfood-content" class="zsnav-content">
	    <div class="zsnav-con-close">
	        <i class="glyphicon glyphicon-chevron-right"></i>
	    </div>
	    <div>
	        食品风险知识
	    </div>
	</div>
	<div id="zscompany-content" class="zsnav-content">
	    <div class="zsnav-con-close">
	        <i class="glyphicon glyphicon-chevron-right"></i>
	    </div>
	    <div>
	        食品安全事件
	    </div>
	</div>
	<div id="zsarea-content" class="zsnav-content">
	    <div class="zsnav-con-close">
	        <i class="glyphicon glyphicon-chevron-right"></i>
	    </div>
	    <div>
	        食品安全监察
	    </div>
	</div>
		
  </div>
</template>

<script type="text/javascript">
// 控制左边列表的弹出
var mini = true;
function toggleSidebar() {
    if (mini) {
        console.log("opening sidebar");
        document.getElementById("mySidebar").style.width = "300px";
        this.mini = false;
    } else {
        console.log("closing sidebar");
        document.getElementById("mySidebar").style.width = "100px";
        this.mini = true;
    }
}
</script>
<script src="../../static/js/jquery.js"></script>
<script src="../../static/js/bootstrap.js"></script>
<script src="../../static/js/bootstrap.min.js"></script>
<script src="../../static/js/common.js"></script>
<script src="../../static/js/init.js"></script>
<script src="../../static/js/jqBootstrapValidation.js"></script>
<script src="../../static/js/plugins.js"></script>
<script src="../../static/js/tubular.js"></script>
<script src="../../static/js/contact_me.js"></script>
<script>
import Nav from '@/components/Nav.vue'
export default {
  name: 'Knowledge',
  components: {
      'v-nav': Nav
  },
  mounted() {
    this.init();
  },
  methods: {
      init(){
         (function() {
      var NavigateBar = function(elementId) {
        this.eId = elementId||'zs-wrap';
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
              currentEl.className = 'zsnav-content';
              //  currentEl.style.top = '0px';
              currentEl.classList.add('zsmove_left');
              console.log("diyici开始之前的evt.currentTarget.id:"+evt.currentTarget.id);
              self.state = 'hasOpened';
              self.currentOpenedEl = currentEl;
            } else {
              self.currentOpenedEl.className = 'zsnav-content';
            //   self.currentOpenedEl.style.top = '0px';
              self.currentOpenedEl.classList.add('zsmove_right');
              currentEl.className = 'zsnav-content';
          //    currentEl.style.top = '0px';
              currentEl.classList.add('zsmove_left');
              self.currentOpenedEl = currentEl; 
            } 
          });
        });


        var navConCloseBarList = document.querySelectorAll('div.zsnav-con-close');
        console.log("有效果吗");
        forEach.call(navConCloseBarList, function(navConCloseBar){
            navConCloseBar.addEventListener('click',function(evt) {
                var currentEl = evt.currentTarget.parentNode;
                
                currentEl.className = 'zsnav-content';
              //   currentEl.style.top = '0px';
                currentEl.classList.add('zsmove_right');
                self.state = 'allClosed';
                var zsf = document.getElementById('zsfood');
                var zsc = document.getElementById('zscompany');
                var zsa = document.getElementById('zsarea');
                zsf.classList.remove('zs-sidebar-item-active');
                zsc.classList.remove('zs-sidebar-item-active');
                zsa.classList.remove('zs-zs-sidebar-item-active');
                console.log(self,evt);
                console.log("nihao");
            });
        });
      };

      NavigateBar.prototype.close = function() {
          this.currentOpenedEl.className = 'zsnav-content';
        //   this.currentOpenedEl.style.top = '0px';
          this.currentOpenedEl.classList.add('zsmove_right');
         // var currentA = document.getElementById(self.eId);
        //  currentA.classList.remove('zs-sidebar-item-active');
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

      $('.zs-sidebar-item').each(function(index){
          $(this).click(function(){
              $(this).addClass('zs-sidebar-item-active').siblings().removeClass('zs-sidebar-item-active');
          });
      });
      }
  }
  
}
</script>

<style>
@import '../../static/css/bootstrap.css';
@import '../../static/css/bootstrap.min.css';
@import '../../static/css/animate.css';
@import '../../static/css/style.css';
@import '../../static/css/zstp.css';
@import '../../static/css/jcfx.css';
@import '../../static/css/pe-icons.css';
@import '../../static/css/font-awesome-4.1.0/css/font-awesome.min.css';
#knowledge {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
@-webkit-keyframes zsmove_right {
			from {
				opacity: 1;
			}
			to {
				opacity: 0;
				-webkit-transform: translateX(120px);
				transform: translateX(120px);
			}
		}
		
		@keyframes zsmove_right {
			from {
				opacity: 1;
			}
			to {
				opacity: 0;
				-webkit-transform: translateX(120px);
				transform: translateX(120px);
			}
		}
		
		@-webkit-keyframes zsmove_left {
			from {
				opacity: 0;
			}
			to {
				opacity: 1;
				-webkit-transform: translateX(-120px);
				transform: translateX(-120px);
			}
		}
		
		@keyframes zsmove_left {
			from {
				opacity: 0;
			}
			to {
				opacity: 1;
				-webkit-transform: translateX(-120px);
				transform: translateX(-120px);
			}
		}
		.zsmove_right {
			-webkit-animation-name            : zsmove_right;
			animation-name            : zsmove_right;
			-webkit-animation-duration        : 1s;
			animation-duration        : 1s;
			-webkit-animation-iteration-count : 1;
			animation-iteration-count : 1;
			-webkit-animation-fill-mode : forwards;
			animation-fill-mode : forwards;
		}
		
		.zsmove_left {
			-webkit-animation-name            : zsmove_left;
			animation-name            : zsmove_left;
			-webkit-animation-duration        : 1s;
			animation-duration        : 1s;
			-webkit-animation-iteration-count : 1;
			animation-iteration-count : 1;
			-webkit-animation-fill-mode : forwards;
			animation-fill-mode : forwards;
    }
   
</style>
