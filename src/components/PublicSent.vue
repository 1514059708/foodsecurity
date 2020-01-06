<style scope>
@import '../../static/css/bootstrap.css';
@import '../../static/css/bootstrap.min.css';
@import '../../static/css/animate.css';
@import '../../static/css/style.css';
@import '../../static/css/yqfx.css';
@import '../../static/css/pe-icons.css';
@import '../../static/css/font-awesome-4.1.0/css/font-awesome.min.css';
@import url("https://api.tiles.mapbox.com/mapbox-gl-js/v0.51.0/mapbox-gl.css");

#public {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body { margin: 0; padding: 0;}
#map { position: absolute; top: 0; bottom: 0; width: 100%; zoom: 1; };
.mypopup {
	max-width: 200px;
	max-height: 300px;
	border-radius: 20px;
}
.mapboxgl-popup {
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    padding: 20px;
	font: 12px/20px 'Helvetica Neue', Arial, Helvetica, sans-serif;
	border-radius: 10px;
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
	display: inline-block;
    margin-top: 0.5em;
    border-radius: 2.5em !important;
    border: none !important;
	background-color: #fff !important;
	margin-right: 5px;
}
#menu {
	position: absolute;
	top: 80px;
	left: 30px;
	border-radius: 40px;
	background: #fff;
	padding: 10px;
	font-family: 'Open Sans', sans-serif;
}
 .mapboxgl-ctrl-top-right {
	  top: auto;
      bottom: 90px !important;
  }
.mapboxgl-ctrl-group > button.mapboxgl-ctrl-compass {
    display: none !important;
}
.yq-index-item a:hover,.yq-index-item a:focus,.yq-index-item a:active,.yq-index-item a.active {
	color: #fff;
	background: #f7a715;
	text-shadow: 1px 1px 3px rgba(0,0,0,.4);
    box-shadow: 0 1.5px 3px rgba(0,0,0,.25);
}
</style>
<template>
  <div id="public">
	<!-- 地图 -->
	<div id='map'></div>
	<div id="menu">
		<input id="streets-v9" type="radio" name="rtoggle" value="streets" checked="checked"/>
		<label for="streets">streets</label>
		<input id="light-v9" type="radio" name="rtoggle" value="light" />
		<label for="light">light</label>
		<input id="dark-v9" type="radio" name="rtoggle" value="dark" />
		<label for="dark">dark</label>
		<input id="outdoors-v9" type="radio" name="rtoggle" value="outdoors" />
		<label for="outdoors">outdoors</label>
		<input id="satellite-v9" type="radio" name="rtoggle" value="satellite" />
		<label for="satellite">satellite</label>
		</div>

<!-- 插件导航 -->
    <v-nav></v-nav>
    <!-- Navigation -->
    <!-- <nav class="navbar navbar-default navbar-shrink bounceInDown"> -->
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
	
	<!-- 舆情分析指标和默认标签--> 
	<div class="yq-index">
		<div class="yq-index-item">
			<a href="#">
				<i class="fa fa-rss" aria-hidden="true"></i>
				舆论热度
			</a>
		</div>
		<div class="yq-index-item">
			<a href="#">
				<i class="fa fa-smile-o" aria-hidden="true"></i>
				正面情感
			</a>
		</div>
		<div class="yq-index-item">
			<a href="#">
				<i class="fa fa-frown-o" aria-hidden="true"></i>
				负面情感
			</a>
		</div>
		<div class="yq-index-default">
			<span>模式:</span>
			<button circle>默认全时</button>
		</div>
	</div>
	
	<!-- 时间轴 --> 
	<div class="yq-timeline">
		<div>这是一个时间轴</div>
	</div>
	
	<!-- 右边弹出框信息：舆情分析可视化模块 --> 
	<div id="com-content">
		<div class="close-icon">
		<span v-on:click="closeContent"><i class="fa fa-times fa-lg" aria-hidden="true"></i></span>
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
					<div class="com-content-basic">
						<div class="com-header clearfix">湖北省</div>
						<div class="com-subheader">
							<span>china/ 纬度: 30°33'北 / 经度: 114°16'东</span>
							<span>当前时间: 10:03 2019-12-31</span> 
						</div>
						<ul class="com-menu clearfix">
							<li><a href="#total">走势图</a></li>
							<li><a href="#negative">情感分析图</a></li>
							<li><a href="#positive">话题列表</a></li>
						</ul>

					</div>
					 舆情分析模块的基础信息，比如地理位置，名称，时间 
					<div class="yq-basic-info">
						<div>武汉市,[117,30],2019-12-10</div>
					</div>
				</div>
				<div id="tab2" class="tab-pane">这是zj的详细信息</div>
				<div id="tab3" class="tab-pane">这是jc的详细信息</div>
			</div>
		</div>  
		
	</div>
  </div>
</template>

<script type="text/javascript">
function closeContent(){
    document.getElementById("com-content").style.display = "none";
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
<!-- 地图 -->
<script src='https://api.mapbox.com/mapbox-gl-js/plugins/mapbox-gl-language/v0.10.1/mapbox-gl-language.js'></script>
	
<script>
import mapboxgl from "mapbox-gl";
import MapboxLanguage from '@mapbox/mapbox-gl-language'
import Nav from '@/components/Nav.vue'
export default {
  name: 'Public',
  components: {
	  'v-nav': Nav
  },
  data() {
    return {
        fullscreenLoading: false
      }
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
	  
	  var layerList = document.getElementById('menu');
	  var inputs = layerList.getElementsByTagName('input');
 
		function switchLayer(layer) {
			var layerId = layer.target.id;
			map.setStyle('mapbox://styles/mapbox/' + layerId);

			map.addControl(new MapboxLanguage({
                defaultLanguage: 'zh'
			}));
			new mapboxgl.Marker().setLngLat([110, 37]).addTo(map);

		}
		
		for (var i = 0; i < inputs.length; i++) {
			inputs[i].onclick = switchLayer;
		}

	  //一个小实例
	map.on('load', function () {
		// Add a layer showing the places.
		map.addLayer({
			"id": "places",
			"type": "symbol",
			"source": {
				"type": "geojson",
				"data": {
					"type": "FeatureCollection",
					"features": [{
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "theatre",
						},
						"geometry": {
							"type": "Point",
							"coordinates": [110, 19]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "theatre"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [112, 38]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "bar"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [111, 25]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "art-gallery"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [113, 30]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "bicycle"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [110, 39]
						}
					}, {
					"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "rocket"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [108, 36]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "music"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [110, 35]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "music"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [100, 30]
						}
					}, {
						"type": "Feature",
						"properties": {
							"description": "<div style='text-align:center'>总微博数量：1234<br />正面微博数量：1000<br />负面微博数量：234</div",
							"icon": "music"
						},
						"geometry": {
							"type": "Point",
							"coordinates": [110, 35.5]
						}
					}]
				}
			},
			"layout": {
			"icon-image": "{icon}-15",
			"icon-allow-overlap": true
			}
		});
		
	

		let popup = new mapboxgl.Popup({closeButton: false});
		//popup.addClassName('mypopup');
		
		var popupinfo = new mapboxgl.Popup();

		new mapboxgl.Marker().setLngLat([110, 37]).addTo(map);
		
	//  鼠标悬浮显示信息
		map.on('mouseenter', 'places', function (e) {
			map.getCanvas().style.cursor = 'pointer';
			var coordinates = e.features[0].geometry.coordinates.slice();
			var description = e.features[0].properties.description;
			 
			// Ensure that if the map is zoomed out such that multiple
			// copies of the feature are visible, the popup appears
			// over the copy being pointed to.
			while (Math.abs(e.lngLat.lng - coordinates[0]) > 180) {
			coordinates[0] += e.lngLat.lng > coordinates[0] ? 360 : -360;
			}
		 
			popup.setLngLat(coordinates)
			.setHTML(description)
			.setMaxWidth("200px")
			.addTo(map);

			popup.addClassName('mypopup');
		}); 
		
		//右侧弹出框弹出的具体信息
		map.on('click','places',function(e){
			var coor = e.features[0].geometry.coordinates.slice();
			var des = e.features[0].properties.description;
			 
			// Ensure that if the map is zoomed out such that multiple
			// copies of the feature are visible, the popup appears
			// over the copy being pointed to.
			while (Math.abs(e.lngLat.lng - coor[0]) > 180) {
			coor[0] += e.lngLat.lng > coor[0] ? 360 : -360;
			}
			if(document.getElementById("com-content").style.display === "block"){
				document.getElementById("com-content").style.display = "none";
			}
			else {
				document.getElementById("com-content").style.display = "block";
			}
			console.log("这是一个弹出框");
			/* popupinfo.setLngLat(coor)
			.setHTML(des)
			.addTo(map); */
		})
		 
		
		// Change it back to a pointer when it leaves.
		map.on('mouseleave', 'places', function () {
			map.getCanvas().style.cursor = '';
			popup.remove();
		});
	});
    //   const language = new MapboxLanguage({ defaultLanguage: "zh" });
    // map.addControl(language);
    map.addControl(new MapboxLanguage({
                defaultLanguage: 'zh'
            }));

	map.addControl(new mapboxgl.NavigationControl());
	
	$('.yq-index-item > a').each(function(index){
          $(this).click(function(){
              $(this).addClass('yq-index-item-active').siblings().removeClass('yq-index-item-active');
          });
      });
	},
	// 右边详情页的关闭按钮
	closeContent: function(event) {
		document.getElementById("com-content").style.display = "none";
	},
	//
	openFullScreen1() {
        this.fullscreenLoading = true;
        setTimeout(() => {
          this.fullscreenLoading = false;
        }, 2000);
	  },
	  
	  
  },
  computed: {
  }
}
</script>


