<style scope>
@import "../../static/css/bootstrap.css";
@import "../../static/css/bootstrap.min.css";
@import "../../static/css/animate.css";
@import "../../static/css/style.css";
@import "../../static/css/jcfx.css";
@import "../../static/css/pe-icons.css";
@import "../../static/css/font-awesome-4.1.0/css/font-awesome.min.css";
@import url("https://api.tiles.mapbox.com/mapbox-gl-js/v0.51.0/mapbox-gl.css");

#control {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
#jcmap {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
    zoom: 1;
}
#jc-menu {
    position: absolute;
    top: 80px;
    left: 30px;
    border-radius: 40px;
    background: #fff;
    padding: 10px;
    font-family: "Open Sans", sans-serif;
}
.nav-content-title {
    font-size: 15px;
    padding-top: 5px;
    font-weight: bold;
}
.block {
    margin: 20px 0;
}

.food-table {
    margin: 0 10px;
    height: 290px;
}

.el-picker-panel {
    margin-left: 20px;
}
.area-province {
    position: absolute;
    top: 130px;
    right: 40px;
    font-weight: bold;
}
.mapboxgl-ctrl-group {
    border: none;
    box-shadow: none !important;
    -webkit-box-shadow: none !important;
    background: transparent;
}
.mapboxgl-ctrl-group > button,
.mapboxgl-ctrl-group > button:hover,
.mapboxgl-ctrl-group > button:focus,
.mapboxgl-ctrl-group > button:focus {
    width: 2.5em;
    height: 2.5em;
    display: inline-block;
    margin-top: 0.5em;
    border-radius: 2.5em !important;
    border: none !important;
    background-color: #fff !important;
    margin-right: 5px;
}
.mapboxgl-ctrl-top-right {
    top: auto;
    bottom: 90px !important;
}
.mapboxgl-ctrl-group > button.mapboxgl-ctrl-compass {
    display: none !important;
}
@-webkit-keyframes move_right {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
        -webkit-transform: translateX(440px);
        transform: translateX(440px);
    }
}

@keyframes move_right {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
        -webkit-transform: translateX(440px);
        transform: translateX(440px);
    }
}

@-webkit-keyframes move_left {
    from {
        opacity: 1;
    }
    to {
        opacity: 0;
        -webkit-transform: translateX(-440px);
        transform: translateX(-440px);
    }
}

@keyframes move_left {
    from {
        opacity: 1;
    }
    to {
        opacity: 0;
        -webkit-transform: translateX(-440px);
        transform: translateX(-440px);
    }
}
.move_right {
    -webkit-animation-name: move_right;
    animation-name: move_right;
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-fill-mode: forwards;
    animation-fill-mode: forwards;
}

.move_left {
    -webkit-animation-name: move_left;
    animation-name: move_left;
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-fill-mode: forwards;
    animation-fill-mode: forwards;
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
    -webkit-animation-name: move_up;
    animation-name: move_up;
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-fill-mode: forwards;
    animation-fill-mode: forwards;
}

/**表格样式 */
.el-table tbody tr:hover > td {
    background-color: rgba(255, 255, 255, 0.3) !important;
}
.el-table {
    /* 表格字体颜色 */
    color: #ccc;
    /* 表格边框颜色 */
    /* height: 370px; */
    /* height: 370px; */
    max-height: 370px;
    background-color:  rgba(0,0,0,.01);
}
/* 表格内背景颜色 */
.el-table th,
.el-table tr,
.el-table td {
    border: 0;
    background-color: rgba(47,50,51,.78);
}
/* 双数行背景颜色 */
.el-table--striped .el-table__body tr.el-table__row--striped td {
    background-color: rgba(33,36,37,.62);
}

/* 删除表格下横线 */
.el-table::before {
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0px;
    border: 0;
}
/* 表格表头字体颜色 
.el-table thead {
    color: white;
    font-weight: 500;
    background-color: rgba(148, 144, 144, 0.3);
}*/
.tebale_card {
    /* background-color: #3f5c6d2c; */
    background-color: transparent;
}

.el-table__expanded-cell {
    /* background-color: #3f5c6d2c; */
    background-color: rgba(0,0,0,.01);;
}
/**分页样式 */
.el-pager {
    color: #ccc;
}
.el-pagination--small button, .el-pagination--small span:not([class*=suffix]) {
    color: #ccc;
}
.el-pagination--small .btn-next, .el-pagination--small .btn-prev {
    border-color: transparent;
    font-size: 12px;
    line-height: 22px;
    height: 22px;
    min-width: 22px;
    color: #ccc;
    background: transparent;
}
.el-pager li {
    background-color: transparent;
}
.el-pager li.active {
    color: #ffc107;
} 
.el-pagination button:disabled {
    color: #ccc;
    background-color: transparent;
}
</style>

<template>
    <div id="control">
        <div id="jcmap"></div>

        <div
            id="mrnu"
            style="position:absolute;top:80px;left:30px;width:350px;height:50px;z-index:1;background:#fff;border-radius:30px;padding:10px;"
        >
            <input id="era" type="radio" name="mapstyle" value="dark-v9" checked="checked" />
            <label for="dark">dark</label>
            <input id="erb" type="radio" name="mapstyle" value="streets-v9" />
            <label for="streets">streets</label>
            <input id="erc" type="radio" name="mapstyle" value="light-v9" />
            <label for="light">light</label>
            <input id="erd" type="radio" name="mapstyle" value="outdoors-v9" />
            <label for="outdoors">outdoors</label>
            <input id="ere" type="radio" name="mapstyle" value="satellite-v9" />
            <label for="satellite">satellite</label>
        </div>
        <div id="echartsBox"></div>

        <!-- 插件导航 -->

        <!-- Navigation 页面右上角导航页 -->
        <nav class="navbar navbar-default navbar-shrink bounceInDown">
            <div class="container">
                <!-- Brand and toggle get grouped for better mobile display -->
                <div class="navbar-header page-scroll">
                    <button
                        type="button"
                        class="navbar-toggle"
                        data-toggle="collapse"
                        data-target="#bs-example-navbar-collapse-1"
                    >
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
                            <input
                                class="search-input"
                                type="search"
                                placeholder="请输入食品名称"
                                autocomplete="off"
                            />
                        </label>
                        <ul class="search-list"></ul>
                        <a class="search-btn">
                            <i class="fa fa-location-arrow" aria-hidden="true"></i>
                        </a>
                    </form>
                </div>
                <v-nav></v-nav>
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
            </div>-->
        </div>
        <div id="jcfood-content" class="nav-content">
            <div class="nav-con-close">
                <i class="glyphicon glyphicon-chevron-left"></i>
            </div>
            <div class="nav-content-title">抽检不合格率前十食品列表</div>
            <div class="block">
                <span class="demonstration">默认年份：</span>
                <el-date-picker v-model="value3" type="year" placeholder="选择年"></el-date-picker>
            </div>
            <div class="food-table">
                <el-table
                    :data="tableData.slice((currentPage-1)*pagesize,currentPage*pagesize)" 
                    :cell-style="jcRowClass"
                    :header-cell-style="jcHeadClass"
                    stripe
                    style="width: 95%; position:absolute;"
                >
                    <el-table-column prop="id" label="序号" width="50"></el-table-column>
                    <el-table-column prop="date" label="不合格率" width="120"></el-table-column>
                    <el-table-column prop="name" label="食品名称" width="120"></el-table-column>
                    <el-table-column prop="address" label="批次号"></el-table-column>
                </el-table>
            </div>
            <div class="jcpage">
                <el-pagination
                    small
                    :page-size="pagesize"
                    :pager-count="5"
                    :current-page="currentPage"
                    @current-change="handleCurrentChange"
                    layout="total, prev, pager, next"
                    :total="tableData.length"
                ></el-pagination>
            </div>
            <!-- <div style="height: 36px"></div>
		<el-button>上一年度</el-button> 
            <div style="height: 70px"></div>-->
        </div>
        <div id="jccompany-content" class="nav-content">
            <div class="nav-con-close">
                <i class="glyphicon glyphicon-chevron-left"></i>
            </div>
            <div class="nav-content-title">全国企业食品抽检可视化</div>
            <div class="block">
                <span class="demonstration">默认年份：</span>
                <el-date-picker v-model="value1" type="year" placeholder="选择年"></el-date-picker>
            </div>
            <div id="scatterMap" style="width:420px;height:320px;" ref="myChart"></div>
            <div id="subChart_Company" style="width:420px;height:220px;"></div>
        </div>
        <div id="jcarea-content" class="nav-content">
            <div class="nav-con-close">
                <i class="glyphicon glyphicon-chevron-left"></i>
            </div>
            <div class="nav-content-title">省份食品安全可视化</div>
            <div class="block">
                <span class="demonstration">默认年份：</span>
                <el-date-picker v-model="value2" type="year" placeholder="选择年"></el-date-picker>
            </div>
            <div id="provinceMap" style="width:420px;height:440px;"></div>
            <div class="area-province">江苏省</div>
            <el-table
                :data="tableDataArea"
                stripe
                size="small"
                style="width: 99.9%; position:absolute;"
            >
                <el-table-column prop="discription" label="评价指标" align="center" width="280"></el-table-column>
                <el-table-column prop="value" label="不合格率" align="center"></el-table-column>
            </el-table>
        </div>

        <!-- 右侧关联信息展开栏  -->
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
import MapboxLanguage from "@mapbox/mapbox-gl-language";
import Nav from "@/components/Nav.vue";
import echarts from "echarts";
require("echarts/map/js/china");
require("echarts/map/js/province/jiangsu");
export default {
    name: "control_index",
    components: {
        "v-nav": Nav
    },
    data() {
        return {
            pagesize: 5,
            currentPage: 1,
            value1: "2018",
            value2: "2018",
            value3: "2018",
            tableData: [
                { id: 1, date: "33%", name: "蒙牛牛奶", address: "2019102112" },
                { id: 2, date: "28%", name: "伊利牛奶", address: "2019102123" },
                {
                    id: 3,
                    date: "26%",
                    name: "旺旺牛奶",
                    address: "2019112490"
                },
                {
                    id: 4,
                    date: "21%",
                    name: "经典牛奶",
                    address: "2019122476"
                },
                { id: 5, date: "33%", name: "蒙牛牛奶", address: "2019102112" },
                { id: 6, date: "28%", name: "伊利牛奶", address: "2019102123" },
                {
                    id: 7,
                    date: "26%",
                    name: "旺旺牛奶",
                    address: "2019112490"
                },
                {
                    id: 8,
                    date: "21%",
                    name: "经典牛奶",
                    address: "2019122476"
                },
                { id: 9, date: "33%", name: "蒙牛牛奶", address: "2019102112" },
                {
                    id: 10,
                    date: "28%",
                    name: "伊利牛奶",
                    address: "2019102123"
                }
            ],
            tableDataArea: [
                {
                    discription: "江苏省年度平均不合格率",
                    value: "20%"
                },
                {
                    discription: "大型企业年度平均不合格率",
                    value: "10%"
                },
                {
                    discription: "中型企业年度平均不合格率",
                    value: "20%"
                },
                {
                    discription: "小型企业度平均不合格率",
                    value: "30%"
                }
            ],
            layerId: "dark-v9"
        };
    },
    mounted() {
        this.init();
    },
    methods: {
        //分页当前所在页数
        handleCurrentChange(val){
            this.currentPage = val;
                    
        },
        // 表头样式设置
        jcHeadClass() {
            return "font-size:12px;text-align: center;line-height: 12px;font-weight:700;color:#ccc;background-color: rgba(33,36,37,.62);";
        },
        // 表格样式设
        jcRowClass() {
            return "font-size:14px;text-align: center;line-height: 14px;";
        },
        // 初始化
        init() {
            mapboxgl.accessToken =
                "pk.eyJ1IjoiY2luZHkwNzkiLCJhIjoiY2p5MW0yM2FmMDNhbzNpcnpoeGVqOXpmYSJ9.zKbdCDdA69t7b3zSWctaRw";
            const jcmap = new mapboxgl.Map({
                container: "jcmap", // container id
                style: "mapbox://styles/mapbox/" + this.layerId, // stylesheet location
                center: [110, 37], // starting position [lng, lat]
                zoom: 3.4 // starting zoom
            });
            var layerList = document.getElementById("mrnu");
            var inputs = layerList.getElementsByTagName("input");
            var _this = this; //this指的是init中的全局变量
            function switchLayer(layer) {
                var layerIdd = layer.target.value;
                console.log("layer.target.value" + layer.target.value);
                _this.layerId = layerIdd;
                jcmap.setStyle("mapbox://styles/mapbox/" + layerIdd);
                jcmap.addControl(
                    new MapboxLanguage({
                        defaultLanguage: "zh"
                    })
                );
                _this.init();
                console.log("地图样式切换:" + layerIdd);
            }
            for (var i = 0; i < inputs.length; i++) {
                inputs[i].onclick = switchLayer;
            }
            jcmap.on("load", function() {
                var layers = jcmap.getStyle().layers;
                // Find the index of the first symbol layer in the jcmap style
                var firstSymbolId;
                for (var i = 0; i < 5; i++) {
                    if (layers[i].type === "symbol") {
                        firstSymbolId = layers[i].id;
                        break;
                    }
                }

                //线段端点
                jcmap.addSource("dot", {
                    type: "geojson",
                    data: {
                        type: "FeatureCollection",
                        features: [
                            {
                                type: "Feature",
                                geometry: {
                                    type: "Point",
                                    coordinates: [115.9387207, 28.6327468]
                                },
                                properties: {
                                    description: "这是悬浮窗的内容1"
                                }
                            },
                            {
                                type: "Feature",
                                geometry: {
                                    type: "Point",
                                    coordinates: [102.83203125, 30.44867368]
                                },
                                properties: {
                                    description: "这是悬浮窗的内容2"
                                }
                            },
                            {
                                type: "Feature",
                                geometry: {
                                    type: "Point",
                                    coordinates: [119.35546875, 25.91852616]
                                },
                                properties: {
                                    description: "这是悬浮窗的内容3"
                                }
                            },
                            {
                                type: "Feature",
                                geometry: {
                                    type: "Point",
                                    coordinates: [113.29101563, 23.09994421]
                                },
                                properties: {
                                    description: "这是悬浮窗的内容4"
                                }
                            },
                            {
                                type: "Feature",
                                geometry: {
                                    type: "Point",
                                    coordinates: [108.39111328, 22.71539002]
                                },
                                properties: {
                                    description: "这是悬浮窗的内容5"
                                }
                            }
                        ]
                    }
                });
                jcmap.addLayer(
                    {
                        id: "point",
                        source: "dot",
                        type: "circle",
                        paint: {
                            "circle-radius": 3,
                            "circle-color": "#007cbf"
                        }
                    },
                    firstSymbolId
                );

                var popup = new mapboxgl.Popup({
                    closeButton: false,
                    closeOnClick: false
                });
                //<!-- 悬浮窗效果 -->
                jcmap.on("mouseenter", "point", function(e) {
                    jcmap.getCanvas().style.cursor = "pointer";

                    var coordinates = e.features[0].geometry.coordinates.slice();
                    var description = e.features[0].properties.description;

                    while (Math.abs(e.lngLat.lng - coordinates[0]) > 180) {
                        coordinates[0] +=
                            e.lngLat.lng > coordinates[0] ? 360 : -360;
                    }

                    popup
                        .setLngLat(coordinates)
                        .setHTML(description)
                        .addTo(jcmap);
                });

                jcmap.on("mouseleave", "point", function() {
                    jcmap.getCanvas().style.cursor = "";
                    popup.remove();
                });
            });

            // 实现全链条的线段
            var geoCoordMap = {
                //所有点的信息
                节点1: [115.9387207, 28.6327468],
                节点2: [102.83203125, 30.44867368],
                节点3: [119.35546875, 25.91852616],
                节点4: [113.29101563, 23.09994421],
                节点5: [108.39111328, 22.71539002]
            };
            // 起点数据中name必须与geoCoordMap中NAME一致, 不然关联不上
            var P1Data = [[{ name: "节点1" }, { name: "节点2" }]];
            var P2Data = [[{ name: "节点2" }, { name: "节点3" }]];
            var P3Data = [
                [{ name: "节点3" }, { name: "节点4" }],
                [{ name: "节点3" }, { name: "节点5" }]
            ];
            var PathDirction = "arrow"; //方向用箭头表示
            //  整合开始-结束地点的经纬度
            var convertData = function(data) {
                var res = [];
                for (var i = 0; i < data.length; i++) {
                    var dataItem = data[i];
                    var fromCoord = geoCoordMap[dataItem[0].name];
                    var toCoord = geoCoordMap[dataItem[1].name];
                    if (fromCoord && toCoord) {
                        res.push([
                            {
                                coord: fromCoord
                            },
                            {
                                coord: toCoord
                            }
                        ]);
                    }
                }
                return res;
            };
            var color = ["#007cbf", "#FFFFA8", "#46bee9"]; //圆圈的颜色，线的颜色，箭头颜色
            // 数据
            var series = [];
            [
                ["节点1", P1Data],
                ["节点2", P2Data],
                ["节点3", P3Data] //全链条4个环节共3个起点
            ].forEach(function(item, i) {
                // 配置
                series.push(
                    {
                        name: item[0],
                        type: "lines",
                        zlevel: 1,
                        effect: {
                            show: true,
                            period: 6, // 特效动画的时间，单位s
                            trailLength: 0.1, // 特效尾迹的长度。取从 0 到 1 的值，数值越大尾迹越长
                            color: "#46bee9", // 移动箭头颜色
                            symbol: PathDirction,
                            symbolSize: 6 // 特效标记的大小
                        },
                        // lineStyle出发到目的地 的线条颜色
                        lineStyle: {
                            normal: {
                                color: color[i],
                                width: 2,
                                curveness: 0.2 //幅度
                            }
                        },
                        data: convertData(item[1]) //开始到结束数据
                    },
                    {
                        //出发地信息
                        name: item[0],
                        type: "lines",
                        zlevel: 2,
                        effect: {
                            show: true,
                            period: 6,
                            trailLength: 0,
                            symbol: PathDirction,
                            symbolSize: 6
                        },
                        lineStyle: {
                            normal: {
                                color: new echarts.graphic.LinearGradient(
                                    0,
                                    0,
                                    0,
                                    1,
                                    [
                                        {
                                            offset: 0,
                                            color: "#FFFFA8" // 出发
                                        },
                                        {
                                            offset: 1,
                                            color: "#58B3CC " // 结束颜色
                                        }
                                    ],
                                    false
                                ),
                                width: 1.5,
                                opacity: 0.4,
                                curveness: 0.2
                            }
                        },
                        data: convertData(item[1])
                    },
                    {
                        // 目的地信息
                        name: item[0],
                        type: "effectScatter",
                        coordinateSystem: "geo",
                        zlevel: 2,
                        rippleEffect: {
                            brushType: "stroke"
                        },
                        label: {
                            normal: {
                                show: true,
                                position: "right",
                                formatter: "{b}"
                            }
                        },
                        symbolSize: 6,
                        itemStyle: {
                            normal: {
                                color: color[i]
                            }
                        },
                        data: convertData(item[1])
                    }
                );
                option = {
                    geo: {
                        map: "china",
                        roam: false,
                        aspectScale: 0.75,
                        zoom: 1.2,
                        label: {
                            normal: {
                                show: false,
                                textStyle: {
                                    color: "#00a0c9"
                                }
                            },
                            emphasis: {
                                show: false,
                                textStyle: {
                                    color: "#00a0c9"
                                }
                            }
                        },
                        itemStyle: {
                            normal: {
                                areaColor: "#0083ce",
                                borderColor: "#0066ba"
                            },
                            emphasis: {
                                borderWidth: 0,
                                borderColor: "#0066ba",
                                areaColor: "#0494e1",
                                shadowColor: "rgba(0, 0, 0, 0.5)"
                            }
                        }
                    },
                    series: series
                };
            });

            // 基于准备好的dom，初始化echarts实例
            var myChart = echarts.init(document.getElementById("echartsBox")); //添加<div id="echartsBox"></div>
            var option = {};
            myChart.setOption(option);
            // echart图表自适应
            window.addEventListener("resize", function() {
                myChart.resize();
            });
            //初始化echarts实例
            const scatterMap = echarts.init(
                document.getElementById("scatterMap")
            );
            //城市经纬度
            const scatterGeo = {
                海门: [121.15, 31.89],
                鄂尔多斯: [109.781327, 39.608266],
                招远: [120.38, 37.35],
                舟山: [122.207216, 29.985295],
                齐齐哈尔: [123.97, 47.33],
                盐城: [120.13, 33.38],
                赤峰: [118.87, 42.28],
                青岛: [120.33, 36.07],
                乳山: [121.52, 36.89],
                金昌: [102.188043, 38.520089],
                泉州: [118.58, 24.93],
                莱西: [120.53, 36.86],
                日照: [119.46, 35.42],
                胶南: [119.97, 35.88],
                南通: [121.05, 32.08],
                拉萨: [91.11, 29.97],
                云浮: [112.02, 22.93],
                梅州: [116.1, 24.55],
                文登: [122.05, 37.2],
                上海: [121.48, 31.22],
                攀枝花: [101.718637, 26.582347],
                威海: [122.1, 37.5],
                承德: [117.93, 40.97],
                厦门: [118.1, 24.46],
                汕尾: [115.375279, 22.786211],
                潮州: [116.63, 23.68],
                丹东: [124.37, 40.13],
                太仓: [121.1, 31.45],
                曲靖: [103.79, 25.51],
                烟台: [121.39, 37.52],
                福州: [119.3, 26.08],
                瓦房店: [121.979603, 39.627114],
                即墨: [120.45, 36.38],
                抚顺: [123.97, 41.97],
                玉溪: [102.52, 24.35],
                张家口: [114.87, 40.82],
                阳泉: [113.57, 37.85],
                莱州: [119.942327, 37.177017],
                湖州: [120.1, 30.86],
                汕头: [116.69, 23.39],
                昆山: [120.95, 31.39],
                宁波: [121.56, 29.86],
                湛江: [110.359377, 21.270708],
                揭阳: [116.35, 23.55],
                荣成: [122.41, 37.16],
                连云港: [119.16, 34.59],
                葫芦岛: [120.836932, 40.711052],
                常熟: [120.74, 31.64],
                东莞: [113.75, 23.04],
                河源: [114.68, 23.73],
                淮安: [119.15, 33.5],
                泰州: [119.9, 32.49],
                南宁: [108.33, 22.84],
                营口: [122.18, 40.65],
                惠州: [114.4, 23.09],
                江阴: [120.26, 31.91],
                蓬莱: [120.75, 37.8],
                韶关: [113.62, 24.84],
                嘉峪关: [98.289152, 39.77313],
                广州: [113.23, 23.16],
                延安: [109.47, 36.6],
                太原: [112.53, 37.87],
                清远: [113.01, 23.7],
                中山: [113.38, 22.52],
                昆明: [102.73, 25.04],
                寿光: [118.73, 36.86],
                盘锦: [122.070714, 41.119997],
                长治: [113.08, 36.18],
                深圳: [114.07, 22.62],
                珠海: [113.52, 22.3],
                宿迁: [118.3, 33.96],
                咸阳: [108.72, 34.36],
                铜川: [109.11, 35.09],
                平度: [119.97, 36.77],
                佛山: [113.11, 23.05],
                海口: [110.35, 20.02],
                江门: [113.06, 22.61],
                章丘: [117.53, 36.72],
                肇庆: [112.44, 23.05],
                大连: [121.62, 38.92],
                临汾: [111.5, 36.08],
                吴江: [120.63, 31.16],
                石嘴山: [106.39, 39.04],
                沈阳: [123.38, 41.8],
                苏州: [120.62, 31.32],
                茂名: [110.88, 21.68],
                嘉兴: [120.76, 30.77],
                长春: [125.35, 43.88],
                胶州: [120.03336, 36.264622],
                银川: [106.27, 38.47],
                张家港: [120.555821, 31.875428],
                三门峡: [111.19, 34.76],
                锦州: [121.15, 41.13],
                南昌: [115.89, 28.68],
                柳州: [109.4, 24.33],
                三亚: [109.511909, 18.252847],
                自贡: [104.778442, 29.33903],
                吉林: [126.57, 43.87],
                阳江: [111.95, 21.85],
                泸州: [105.39, 28.91],
                西宁: [101.74, 36.56],
                宜宾: [104.56, 29.77],
                呼和浩特: [111.65, 40.82],
                成都: [104.06, 30.67],
                大同: [113.3, 40.12],
                镇江: [119.44, 32.2],
                桂林: [110.28, 25.29],
                张家界: [110.479191, 29.117096],
                宜兴: [119.82, 31.36],
                北海: [109.12, 21.49],
                西安: [108.95, 34.27],
                金坛: [119.56, 31.74],
                东营: [118.49, 37.46],
                牡丹江: [129.58, 44.6],
                遵义: [106.9, 27.7],
                绍兴: [120.58, 30.01],
                扬州: [119.42, 32.39],
                常州: [119.95, 31.79],
                潍坊: [119.1, 36.62],
                重庆: [106.54, 29.59],
                台州: [121.420757, 28.656386],
                南京: [118.78, 32.04],
                滨州: [118.03, 37.36],
                贵阳: [106.71, 26.57],
                无锡: [120.29, 31.59],
                本溪: [123.73, 41.3],
                克拉玛依: [84.77, 45.59],
                渭南: [109.5, 34.52],
                马鞍山: [118.48, 31.56],
                宝鸡: [107.15, 34.38],
                焦作: [113.21, 35.24],
                句容: [119.16, 31.95],
                北京: [116.46, 39.92],
                徐州: [117.2, 34.26],
                衡水: [115.72, 37.72],
                包头: [110, 40.58],
                绵阳: [104.73, 31.48],
                乌鲁木齐: [87.68, 43.77],
                枣庄: [117.57, 34.86],
                杭州: [120.19, 30.26],
                淄博: [118.05, 36.78],
                鞍山: [122.85, 41.12],
                溧阳: [119.48, 31.43],
                库尔勒: [86.06, 41.68],
                安阳: [114.35, 36.1],
                开封: [114.35, 34.79],
                济南: [117, 36.65],
                德阳: [104.37, 31.13],
                温州: [120.65, 28.01],
                九江: [115.97, 29.71],
                邯郸: [114.47, 36.6],
                临安: [119.72, 30.23],
                兰州: [103.73, 36.03],
                沧州: [116.83, 38.33],
                临沂: [118.35, 35.05],
                南充: [106.110698, 30.837793],
                天津: [117.2, 39.13],
                富阳: [119.95, 30.07],
                泰安: [117.13, 36.18],
                诸暨: [120.23, 29.71],
                郑州: [113.65, 34.76],
                哈尔滨: [126.63, 45.75],
                聊城: [115.97, 36.45],
                芜湖: [118.38, 31.33],
                唐山: [118.02, 39.63],
                平顶山: [113.29, 33.75],
                邢台: [114.48, 37.05],
                德州: [116.29, 37.45],
                济宁: [116.59, 35.38],
                荆州: [112.239741, 30.335165],
                宜昌: [111.3, 30.7],
                义乌: [120.06, 29.32],
                丽水: [119.92, 28.45],
                洛阳: [112.44, 34.7],
                秦皇岛: [119.57, 39.95],
                株洲: [113.16, 27.83],
                石家庄: [114.48, 38.03],
                莱芜: [117.67, 36.19],
                常德: [111.69, 29.05],
                保定: [115.48, 38.85],
                湘潭: [112.91, 27.87],
                金华: [119.64, 29.12],
                岳阳: [113.09, 29.37],
                长沙: [113, 28.21],
                衢州: [118.88, 28.97],
                廊坊: [116.7, 39.53],
                菏泽: [115.480656, 35.23375],
                合肥: [117.27, 31.86],
                武汉: [114.31, 30.52],
                大庆: [125.03, 46.58]
            };
            //城市数据
            const scatterVal = [
                { name: "海门", value: 9 },
                { name: "鄂尔多斯", value: 12 },
                { name: "招远", value: 12 },
                { name: "舟山", value: 12 },
                { name: "齐齐哈尔", value: 14 },
                { name: "盐城", value: 15 },
                { name: "赤峰", value: 16 },
                { name: "青岛", value: 18 },
                { name: "乳山", value: 18 },
                { name: "金昌", value: 19 },
                { name: "泉州", value: 21 },
                { name: "莱西", value: 21 },
                { name: "日照", value: 21 },
                { name: "胶南", value: 22 },
                { name: "南通", value: 23 },
                { name: "拉萨", value: 24 },
                { name: "云浮", value: 24 },
                { name: "梅州", value: 25 },
                { name: "文登", value: 25 },
                { name: "上海", value: 25 },
                { name: "攀枝花", value: 25 },
                { name: "威海", value: 25 },
                { name: "承德", value: 25 },
                { name: "厦门", value: 26 },
                { name: "汕尾", value: 26 },
                { name: "潮州", value: 26 },
                { name: "丹东", value: 27 },
                { name: "太仓", value: 27 },
                { name: "曲靖", value: 27 },
                { name: "烟台", value: 28 },
                { name: "福州", value: 29 },
                { name: "瓦房店", value: 30 },
                { name: "即墨", value: 30 },
                { name: "抚顺", value: 31 },
                { name: "玉溪", value: 31 },
                { name: "张家口", value: 31 },
                { name: "阳泉", value: 31 },
                { name: "莱州", value: 32 },
                { name: "湖州", value: 32 },
                { name: "汕头", value: 32 },
                { name: "昆山", value: 33 },
                { name: "宁波", value: 33 },
                { name: "湛江", value: 33 },
                { name: "揭阳", value: 34 },
                { name: "荣成", value: 34 },
                { name: "连云港", value: 35 },
                { name: "葫芦岛", value: 35 },
                { name: "常熟", value: 36 },
                { name: "东莞", value: 36 },
                { name: "河源", value: 36 },
                { name: "淮安", value: 36 },
                { name: "泰州", value: 36 },
                { name: "南宁", value: 37 },
                { name: "营口", value: 37 },
                { name: "惠州", value: 37 },
                { name: "江阴", value: 37 },
                { name: "蓬莱", value: 37 },
                { name: "韶关", value: 38 },
                { name: "嘉峪关", value: 38 },
                { name: "广州", value: 38 },
                { name: "延安", value: 38 },
                { name: "太原", value: 39 },
                { name: "清远", value: 39 },
                { name: "中山", value: 39 },
                { name: "昆明", value: 39 },
                { name: "寿光", value: 40 },
                { name: "盘锦", value: 40 },
                { name: "长治", value: 41 },
                { name: "深圳", value: 41 },
                { name: "珠海", value: 42 },
                { name: "宿迁", value: 43 },
                { name: "咸阳", value: 43 },
                { name: "铜川", value: 44 },
                { name: "平度", value: 44 },
                { name: "佛山", value: 44 },
                { name: "海口", value: 44 },
                { name: "江门", value: 45 },
                { name: "章丘", value: 45 },
                { name: "肇庆", value: 46 },
                { name: "大连", value: 47 },
                { name: "临汾", value: 47 },
                { name: "吴江", value: 47 },
                { name: "石嘴山", value: 49 },
                { name: "沈阳", value: 50 },
                { name: "苏州", value: 50 },
                { name: "茂名", value: 50 },
                { name: "嘉兴", value: 51 },
                { name: "长春", value: 51 },
                { name: "胶州", value: 52 },
                { name: "银川", value: 52 },
                { name: "张家港", value: 52 },
                { name: "三门峡", value: 53 },
                { name: "锦州", value: 54 },
                { name: "南昌", value: 54 },
                { name: "柳州", value: 54 },
                { name: "三亚", value: 54 },
                { name: "自贡", value: 56 },
                { name: "吉林", value: 56 },
                { name: "阳江", value: 57 },
                { name: "泸州", value: 57 },
                { name: "西宁", value: 57 },
                { name: "宜宾", value: 58 },
                { name: "呼和浩特", value: 58 },
                { name: "成都", value: 58 },
                { name: "大同", value: 58 },
                { name: "镇江", value: 59 },
                { name: "桂林", value: 59 },
                { name: "张家界", value: 59 },
                { name: "宜兴", value: 59 },
                { name: "北海", value: 60 },
                { name: "西安", value: 61 },
                { name: "金坛", value: 62 },
                { name: "东营", value: 62 },
                { name: "牡丹江", value: 63 },
                { name: "遵义", value: 63 },
                { name: "绍兴", value: 63 },
                { name: "扬州", value: 64 },
                { name: "常州", value: 64 },
                { name: "潍坊", value: 65 },
                { name: "重庆", value: 66 },
                { name: "台州", value: 67 },
                { name: "南京", value: 67 },
                { name: "滨州", value: 70 },
                { name: "贵阳", value: 71 },
                { name: "无锡", value: 71 },
                { name: "本溪", value: 71 },
                { name: "克拉玛依", value: 72 },
                { name: "渭南", value: 72 },
                { name: "马鞍山", value: 72 },
                { name: "宝鸡", value: 72 },
                { name: "焦作", value: 75 },
                { name: "句容", value: 75 },
                { name: "北京", value: 79 },
                { name: "徐州", value: 79 },
                { name: "衡水", value: 80 },
                { name: "包头", value: 80 },
                { name: "绵阳", value: 80 },
                { name: "乌鲁木齐", value: 84 },
                { name: "枣庄", value: 84 },
                { name: "杭州", value: 84 },
                { name: "淄博", value: 85 },
                { name: "鞍山", value: 86 },
                { name: "溧阳", value: 86 },
                { name: "库尔勒", value: 86 },
                { name: "安阳", value: 90 },
                { name: "开封", value: 90 },
                { name: "济南", value: 92 },
                { name: "德阳", value: 93 },
                { name: "温州", value: 95 },
                { name: "九江", value: 96 },
                { name: "邯郸", value: 98 },
                { name: "临安", value: 99 },
                { name: "兰州", value: 99 },
                { name: "沧州", value: 100 },
                { name: "临沂", value: 103 },
                { name: "南充", value: 104 },
                { name: "天津", value: 105 },
                { name: "富阳", value: 106 },
                { name: "泰安", value: 112 },
                { name: "诸暨", value: 112 },
                { name: "郑州", value: 113 },
                { name: "哈尔滨", value: 114 },
                { name: "聊城", value: 116 },
                { name: "芜湖", value: 117 },
                { name: "唐山", value: 119 },
                { name: "平顶山", value: 119 },
                { name: "邢台", value: 119 },
                { name: "德州", value: 120 },
                { name: "济宁", value: 120 },
                { name: "荆州", value: 127 },
                { name: "宜昌", value: 130 },
                { name: "义乌", value: 132 },
                { name: "丽水", value: 133 },
                { name: "洛阳", value: 134 },
                { name: "秦皇岛", value: 136 },
                { name: "株洲", value: 143 },
                { name: "石家庄", value: 147 },
                { name: "莱芜", value: 148 },
                { name: "常德", value: 152 },
                { name: "保定", value: 153 },
                { name: "湘潭", value: 154 },
                { name: "金华", value: 157 },
                { name: "岳阳", value: 169 },
                { name: "长沙", value: 175 },
                { name: "衢州", value: 177 },
                { name: "廊坊", value: 193 },
                { name: "菏泽", value: 194 },
                { name: "合肥", value: 229 },
                { name: "武汉", value: 273 },
                { name: "大庆", value: 279 }
            ];
            //数据转换，转换后的格式：[{name: 'cityName', value: [lng, lat, val]}, {...}]
            const convertScatterData = function(data) {
                let res = [];
                for (let i = 0; i < data.length; i++) {
                    let geoCoord = scatterGeo[data[i].name];
                    if (geoCoord) {
                        res.push({
                            name: data[i].name,
                            value: geoCoord.concat(data[i].value)
                        });
                    }
                }
                return res;
            };
            //地图配置项
            const sactterMapOpt = {
                title: {
                    //text: '全国企业',
                    x: "center",
                    textStyle: {
                        color: "#fff"
                    }
                },
                legend: {
                    data: ["PM2.5"], //与series的name属性对应
                    orient: "vertical",
                    y: "bottom",
                    x: "right",
                    textStyle: {
                        color: "#fff"
                    }
                },
                tooltip: {
                    trigger: "item",
                    formatter: function(params) {
                        return params.name + " : " + params.value[2];
                    }
                },
                visualMap: {
                    min: 0,
                    max: 200,
                    calculable: true,
                    inRange: {
                        color: ["#50a3ba", "#eac736", "#d94e5d"]
                    },
                    textStyle: {
                        color: "#fff"
                    }
                },
                geo: {
                    map: "china",
                    roam: false, //开启鼠标缩放和漫游
                    zoom: 1, //地图缩放级别
                    selectedMode: false, //选中模式：single | multiple
                    left: 0,
                    right: 0,
                    top: 0,
                    bottom: 0,
                    layoutCenter: ["50%", "50%"], //设置后left/right/top/bottom等属性无效
                    layoutSize: "100%",
                    label: {
                        emphasis: {
                            show: false
                        }
                    },
                    itemStyle: {
                        normal: {
                            areaColor: "#101f32",
                            borderWidth: 1.1,
                            borderColor: "#43d0d6"
                        },
                        emphasis: {
                            areaColor: "#069"
                        }
                    }
                },
                series: [
                    {
                        name: "PM2.5",
                        type: "scatter",
                        coordinateSystem: "geo",
                        symbolSize: 12,
                        label: {
                            normal: {
                                show: false
                            },
                            emphasis: {
                                show: false
                            }
                        },
                        itemStyle: {
                            emphasis: {
                                borderColor: "#fff",
                                borderWidth: 1
                            }
                        },
                        data: convertScatterData(scatterVal)
                    }
                ]
            };
            //渲染报表
            scatterMap.setOption(sactterMapOpt);

            //引入
            //var echarts = require('echarts');

            // 基于准备好的dom，初始化echarts实例
            var myChart = echarts.init(
                document.getElementById("subChart_Company")
            );

            // 绘制图表
            myChart.setOption({
                title: {
                    text: "2018重点省份不合格公司数量统计",
                    left: "17%",
                    right: "20%",
                    textStyle: {
                        textSize: "10",
                        color: "#ffffff"
                    }
                },
                tooltip: {},
                xAxis: {
                    data: [
                        "北京市",
                        "四川省",
                        "湖北省",
                        "河南省",
                        "贵州省",
                        "山东省"
                    ],
                    axisLabel: {
                        show: true,
                        textStyle: {
                            color: "#ffffff"
                        }
                    }
                },
                yAxis: {
                    axisLabel: {
                        show: true,
                        textStyle: {
                            color: "#ffffff"
                        }
                    }
                },
                series: [
                    {
                        name: "不合格公司数量",
                        type: "bar",
                        data: [5, 20, 36, 10, 10, 20],
                        itemStyle: {
                            normal: {
                                color: "#d94e5d"
                            }
                        }
                    }
                ]
            });
            // window.onresize = function(){
            // 	this.myChart.resize()
            // 	}

            //初始化echarts实例
            const provinceMap = echarts.init(
                document.getElementById("provinceMap")
            );
            const provinceMapOpt = {
                geo: {
                    map: "江苏",
                    roam: false, //开启鼠标缩放和漫游
                    zoom: 1, //地图缩放级别
                    selectedMode: false, //选中模式：single | multiple
                    left: 0,
                    right: 0,
                    top: 0,
                    bottom: 0,
                    layoutCenter: ["50%", "50%"], //设置后left/right/top/bottom等属性无效
                    layoutSize: "100%", //保持地图宽高比
                    label: {
                        emphasis: {
                            show: true,
                            color: "#f19000"
                        }
                    },
                    itemStyle: {
                        normal: {
                            areaColor: "#101f32",
                            borderWidth: 1.1,
                            borderColor: "#43d0d6"
                        },
                        emphasis: {
                            areaColor: "#069"
                        }
                    }
                }
            };
            provinceMap.setOption(provinceMapOpt);
            //   const language = new MapboxLanguage({ defaultLanguage: "zh" });
            // jcmap.addControl(language);
            jcmap.addControl(
                new MapboxLanguage({
                    defaultLanguage: "zh"
                })
            );

            jcmap.addControl(new mapboxgl.NavigationControl());

            (function() {
                var NavigateBar = function(elementId) {
                    this.eId = elementId || "jc-wrap";
                    this.el = document.getElementById(this.eId);
                    this.el.addEventListener("click", function(evt) {
                        evt.stopPropagation();
                    });
                    this.state = "allClosed"; //hasOpened
                    this.currentOpenedEl = null;

                    //使用jquery就更方便使用Delegation
                    var forEach = Array.prototype.forEach;
                    var self = this;
                    console.log("未开始之前的self.state:" + self.state);
                    var navigatorList = document.querySelectorAll(
                        "#" + this.eId + " > div"
                    );
                    forEach.call(navigatorList, function(navigator) {
                        navigator.addEventListener("click", function(evt) {
                            var currentEl = document.getElementById(
                                evt.currentTarget.id + "-content"
                            );
                            var currentA = document.getElementById(
                                evt.currentTarget.id
                            );
                            if (self.state === "allClosed") {
                                currentEl.className = "nav-content";
                                //  currentEl.style.top = '0px';
                                currentEl.classList.add("move_right");
                                console.log(
                                    "diyici开始之前的evt.currentTarget.id:" +
                                        evt.currentTarget.id
                                );
                                self.state = "hasOpened";
                                self.currentOpenedEl = currentEl;
                            } else {
                                self.currentOpenedEl.className = "nav-content";
                                //   self.currentOpenedEl.style.top = '0px';
                                self.currentOpenedEl.classList.add("move_left");
                                currentEl.className = "nav-content";
                                //    currentEl.style.top = '0px';
                                currentEl.classList.add("move_right");
                                self.currentOpenedEl = currentEl;
                            }
                        });
                    });

                    var navConCloseBarList = document.querySelectorAll(
                        ".nav-content > div.nav-con-close"
                    );
                    forEach.call(navConCloseBarList, function(navConCloseBar) {
                        navConCloseBar.addEventListener("click", function(evt) {
                            var currentEl = evt.currentTarget.parentNode;

                            currentEl.className = "nav-content";
                            //   currentEl.style.top = '0px';
                            currentEl.classList.add("move_left");
                            self.state = "allClosed";
                            var jcf = document.getElementById("jcfood");
                            var jcc = document.getElementById("jccompany");
                            var jca = document.getElementById("jcarea");
                            jcf.classList.remove("sidebar-item-active");
                            jcc.classList.remove("sidebar-item-active");
                            jca.classList.remove("sidebar-item-active");
                            console.log(self, evt);
                        });
                    });
                };

                NavigateBar.prototype.close = function() {
                    this.currentOpenedEl.className = "nav-content";
                    //   this.currentOpenedEl.style.top = '0px';
                    this.currentOpenedEl.classList.add("move_left");
                    // var currentA = document.getElementById(self.eId);
                    //  currentA.classList.remove('sidebar-item-active');
                    console.log("this.currentOpenedEl:" + this.currentOpenedEl);
                    this.state = "allClosed";
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
            this.el.style.left = '-440px';
            this.el.className = 'move_right';
            this.closeBarEl.style.left = '160px';
            this.closeBarEl.className = 'move_left';
            this.state = 'opened';
        };
        var sideBar = new SideBar();  */
            })();

            $(".sidebar-item").each(function(index) {
                $(this).click(function() {
                    $(this)
                        .addClass("sidebar-item-active")
                        .siblings()
                        .removeClass("sidebar-item-active");
                });
            });
        }
    },
    computed: {}
};
</script>

