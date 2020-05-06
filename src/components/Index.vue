<template>
  <div id="index" class="index">
    <!-- <div class="preloader">
        <div class="preloader-img">
        	<img src="../../static/image/loading-bars.svg" width="100" alt="Loading icon" />
        </div>
    </div> -->
    <!-- 插件导航 -->
    
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
            <v-nav></v-nav>
            <!-- /.navbar-collapse -->
        </div>
        <!-- /.container-fluid -->
    </nav>
    <div id="search-wrapper">
        <button type="button" class="close">×</button>
        <form>
            <input type="search" value="" placeholder="type keyword(s) here" />
            <button type="submit" class="btn btn-primary">Search</button>
        </form>
    </div>

    <!-- Header -->
    <!--<header id="headerwrap" class="fullheight">
        <div class="container">
            <div class="intro-text">
                <div class="intro-lead-in wow bounceInDown" data-wow-delay="0.5s">We Can Help You <span class="wodry">Create|Design|Profit</span></div>
                <div class="intro-heading wow bounceInUp" data-wow-delay="1s">SMASHCO <span class="thin">N.Y.C.</span></div>
                <a href="#about-us" class="page-scroll btn btn-xl btn-negative  wow bounceInDown" data-wow-delay="2s">Tell Me More <i class="fa fa-angle-down fa-2x"></i></a>
            </div>
        </div>
    </header> -->

    <!-- 轮播图片 -->
    <div class="block">
        <span class="demonstration">默认 Hover 指示器触发</span>
        <el-carousel height="150px">
        <el-carousel-item v-for="item in 4" :key="item">
            <h3 class="small">{{ item }}</h3>
        </el-carousel-item>
        </el-carousel>
    </div>
    <!-- About Section -->
    <section id="about-us">
        <div class="section-inner">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12 text-center wow fadeInDown">
                        <h2 class="section-heading"><strong>About</strong> Us</h2>
                        <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <div class="tlinks">Collect from <a href="http://www.cssmoban.com/" >建站模板</a></div>

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
<script>
import Nav from '@/components/Nav.vue'
export default {
  name: 'Index',
  components: {
      'v-nav': Nav
  }
}
</script>

<style scope>
@import '../../static/css/bootstrap.css';
@import '../../static/css/bootstrap.min.css';
@import '../../static/css/animate.css';
@import '../../static/css/style.css';
@import '../../static/css/pe-icons.css';
@import '../../static/css/font-awesome-4.1.0/css/font-awesome.min.css';
#index {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.map-overlay {
    font: 12px/20px 'Helvetica Neue', Arial, Helvetica, sans-serif;
    position: absolute;
    width: 25%;
    top: 0;
    left: 0;
    padding: 10px;
    }
        
    .map-overlay .map-overlay-inner {
    background-color: #fff;
    box-shadow:0 1px 2px rgba(0, 0, 0, 0.20);
    border-radius: 3px;
    padding: 10px;
    margin-bottom: 10px;
    }
        
    .map-overlay h2 {
    line-height: 24px;
    display: block;
    margin: 0 0 10px;
    }
        
    .map-overlay .legend .bar {
    height: 10px;
    width: 100%;
    background: linear-gradient(to right, #FCA107, #7F3121);
    }
        
    .map-overlay input {
    background-color: transparent;
    display: inline-block;
    width: 100%;
    position: relative;
    margin: 0;
    cursor: ew-resize;
    }
    .block,.el-carousel--horizontal {
        margin-top: 50px;
    }
    .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  
  .el-carousel__item:nth-child(2n+1) {
     background-color: #d3dce6;
  }

  .mapboxgl-ctrl-top-right {
      bottom: 0 !important;
  }
#knowledge .mapboxgl-ctrl-group > button.mapboxgl-ctrl-compass {
    display: none !important;
}
</style>
