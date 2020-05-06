<style scope>
@import "../../static/css/bootstrap.css";
@import "../../static/css/bootstrap.min.css";
@import "../../static/css/animate.css";
@import "../../static/css/style.css";
@import "../../static/css/yqfx.css";
@import "../../static/css/pe-icons.css";
@import "../../static/css/font-awesome-4.1.0/css/font-awesome.min.css";
@import "../../static/css/yq-iconfont/iconfont.css";
@import url("https://api.tiles.mapbox.com/mapbox-gl-js/v0.51.0/mapbox-gl.css");

#public {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
body {
    margin: 0;
    padding: 0;
}
#map {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
    zoom: 1;
}
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
    font: 12px/20px "Helvetica Neue", Arial, Helvetica, sans-serif;
    border-radius: 10px;
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
#menu {
    position: absolute;
    top: 80px;
    left: 30px;
    border-radius: 40px;
    background: #fff;
    padding: 10px;
    font-family: "Open Sans", sans-serif;
}
.mapboxgl-ctrl-top-right {
    top: auto;
    bottom: 90px !important;
}
.mapboxgl-ctrl-group > button.mapboxgl-ctrl-compass {
    display: none !important;
}

.yq-index-item a.active {
    color: #fff;
    background: #f7a715;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.4);
    box-shadow: 0 1.5px 3px rgba(0, 0, 0, 0.25);
}
.iconfont {
    width: 1.5em;
    fill: currentColor;
    font-size: 14px;
    padding: 0.1em !important;
    display: inline-block;
}
.icon {
    font-size: 10px;
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
    max-height: 300px;
    background-color: rgba(0, 0, 0, 0.01);
}
/* 表格内背景颜色 */
.el-table th,
.el-table tr,
.el-table td {
    border: 0;
    background-color: rgba(47, 50, 51, 0.78);
}
/* 双数行背景颜色 */
.el-table--striped .el-table__body tr.el-table__row--striped td {
    background-color: rgba(33, 36, 37, 0.62);
}

/* 删除表格下横线 */
.el-table::before {
    left: 0;
    bottom: 0;
    width: 100%;
    height: 0px;
    border: 0;
}
/* 表格表头字体颜色  */
.el-table thead {
    color: white;
    font-weight: 500;
    background-color: rgba(148, 144, 144, 0.3);
    font-family: Helvetica Neue, Arial, Helvetica, sans-serif;
}
.tebale_card {
    /* background-color: #3f5c6d2c; */
    background-color: transparent;
}

.el-table__expanded-cell {
    /* background-color: #3f5c6d2c; */
    background-color: rgba(0, 0, 0, 0.01);
}

.el-table td,
.el-table th {
    padding: 10px 0;
}
/**分页样式 */
.el-pager {
    color: #ccc;
}
.el-pagination--small button,
.el-pagination--small span:not([class*="suffix"]) {
    color: #ccc;
}
.el-pagination--small .btn-next,
.el-pagination--small .btn-prev {
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
/** 模糊查询的样式*/
.yq-search-scrollbar {
    -webkit-box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
    box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    border: 1px solid #e4e7ed;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    background-color: #fff;
    overflow: hidden;
    position: absolute;
    top: 55px;
    width: 17.3em;
}
#yq-search-scrollbar.closed{
    display: none;
}
.yq-search-fuzzy {
    height: 100%;
    width: 100%;
    max-height: 280px;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
}
.yq-search-fuzzy ul {
    margin: 0;
    padding: 0;
    display: block;
    list-style-type: disc;
    -webkit-margin-before: 1em;
    margin-block-start: 1em;
    -webkit-margin-after: 1em;
    margin-block-end: 1em;
    -webkit-margin-start: 0px;
    margin-inline-start: 0px;
    -webkit-margin-end: 0px;
    margin-inline-end: 0px;
}
.yq-search-fuzzy li {
    padding: 0 20px;
    margin: 0;
    line-height: 34px;
    cursor: pointer;
    color: #606266;
    font-size: 14px;
    list-style: none;
    white-space: nowrap;
    cursor: pointer;
    text-align: left;
}
.yq-search-fuzzy li i {
    padding-right: 5px;
}
.yq-search-fuzzy li:hover {
    background-color: rgba(0, 0, 0, 0.1);
}
</style>
<template>
    <div id="public">
        <!-- 地图 -->
        <div id="map"></div>
        <div id="menu">
            <input id="dark-v9" type="radio" name="rtoggle" value="dark" checked="checked" />
            <label for="dark">dark</label>
            <input id="streets-v9" type="radio" name="rtoggle" value="streets" />
            <label for="streets">streets</label>
            <input id="light-v9" type="radio" name="rtoggle" value="light" />
            <label for="light">light</label>
            <input id="outdoors-v9" type="radio" name="rtoggle" value="outdoors" />
            <label for="outdoors">outdoors</label>
            <input id="satellite-v9" type="radio" name="rtoggle" value="satellite" />
            <label for="satellite">satellite</label>
        </div>

        <!-- 插件导航 -->

        <!-- Navigation -->
        <!-- <nav class="navbar navbar-default navbar-shrink bounceInDown"> -->
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
                    <form id="form-inline" class="form-inline my-2 my-lg-0 ty-search">
                        <h1>
                            <a href="./">食品安全</a>
                        </h1>
                        <!-- 搜索模块 -->
                        <label for="search-food">
                            <i class="fa fa-search" aria-hidden="true"></i>
                            <input
                                class="search-input"
                                type="search"
                                placeholder="请输入食品名称"
                                v-model="searchVal"
                                v-on:focus="yqfocus()"
                                v-on:blur="yqblur()"
                                autocomplete="off"
                            />
                        </label>
                        <ul id="search-list" class="search-list closed">
                            <li
                                v-for="(item,index) in yqsearch"
                                :key="index"
                                @click="chooseYqSearch(item)"
                            >
                                <a>
                                    <h3>
                                        <b>{{ selectSearch }}</b>
                                    </h3>
                                    <span>
                                        时间：{{ item.startdate }}——{{ item.enddate }}
                                        <br />地区：{{item.space}}
                                    </span>
                                </a>
                            </li>
                        </ul>

                        <!-- 模糊搜索列表 -->
                        <div id="yq-search-scrollbar" class="yq-search-scrollbar closed">
                            <div class="yq-search-fuzzy">
                                <ul class="yq-fuzzy-list" v-show="yqfuzzy.length">
                                    <li
                                        v-for="(item,index) in yqfuzzy"
                                        :key="index"
                                        @click="chooseYqFuzzy(item)"
                                    >
                                        <span>
                                            <i class="fa fa-info-circle" aria-hidden="true"></i>
                                            {{ item.event_name }}
                                        </span>
                                    </li>
                                </ul>
                                <ul class="yq-fuzzy-list" v-show="!yqfuzzy.length">
                                    <li>
                                        <span>暂无数据，请输入其他关键词</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                        <a class="search-btn">
                            <i class="fa fa-location-arrow" aria-hidden="true"></i>
                        </a>

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

        <!-- 舆情分析指标和默认标签-->
        <div class="yq-index">
            <div class="yq-index-item" id="layer">
                <a id="total" href="#" class="active">
                    <i class="iconfont icon-fire" aria-hidden="true"></i>舆论热度
                </a>
                <a id="pos" href="#">
                    <i class="fa fa-smile-o" aria-hidden="true"></i>
                    正面情感
                </a>
                <a id="neg" href="#">
                    <i class="fa fa-frown-o" aria-hidden="true"></i>
                    负面情感
                </a>
            </div>
        </div>

        <!-- 时间轴 -->
        <div class="yq-timeline">
            <v-timer
                :options="options"
                :dateTimes="dateTimes"
                :startTime="startTime"
                :endTime="endTime"
                @getDateFun="getDateFun"
                @getTimeUnit="getTimeUnit"
                :interval="interval"
            ></v-timer>
        </div>

        <!-- 右边弹出框信息：舆情分析可视化模块 -->
        <div id="yq-sidebar">
            <div id="yq-wrap">
                <div id="yqfood" class="yq-sidebar-item">
                    <div>舆情分析数据</div>
                </div>
                <div id="yqcompany" class="yq-sidebar-item">
                    <div>食品风险知识</div>
                </div>
                <div id="yqarea" class="yq-sidebar-item">
                    <div>食品安全监察</div>
                </div>
            </div>
        </div>

        <!-- 舆情数据模块 -->
        <div id="yqfood-content" class="yqnav-content">
            <p class="modulebox_title__3Rw-h">
                <span>
                    <svg
                        style="cursor:pointer"
                        viewBox="0 0 1024 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="4023"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M976 672c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.08-0.208 0.08L512 860.048 66.784 675.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a48 48 0 0 0-36.704 88.656v0.016l463.584 191.824a1.12 1.12 0 0 0 0.208 0.08l0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 672zM29.664 348.336v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.456 47.456 0 0 0 36.672 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48.048 48.048 0 0 0 1024 304a48 48 0 0 0-29.648-44.336v-0.016L530.784 67.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a47.744 47.744 0 0 0-36.688-0.016l-0.016-0.016-0.208 0.08a1.12 1.12 0 0 1-0.208 0.08L29.648 259.648v0.016A48 48 0 0 0 0 304a48 48 0 0 0 29.664 44.336zM976 464c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.096a1.12 1.12 0 0 1-0.208 0.08L512 652.048 66.784 467.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.096-0.016 0.016a48 48 0 0 0-36.704 88.672v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 464z"
                            fill="#ffffff"
                            p-id="4024"
                        />
                    </svg>
                    <span>舆情分析数据</span>
                </span>
                <span class="modulebox_hidebtn__QHdrj">
                    <svg
                        viewBox="0 0 1045 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="5501"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M282.517333 213.376l-45.354666 45.162667L489.472 512 237.162667 765.461333l45.354666 45.162667L534.613333 557.354667l252.096 253.269333 45.354667-45.162667-252.288-253.44 252.288-253.482666-45.354667-45.162667L534.613333 466.624l-252.096-253.226667z"
                            p-id="5502"
                        />
                    </svg>
                </span>
            </p>
            <div class="yq-zl">
                <div
                    id="city"
                    style="font-weight:bold;font-family: Helvetica Neue,Arial,Helvetica,sans-serif"
                >中国</div>
                <div id="description" style="padding: 1px 1px 10px 1px;color:#fff">
                    <i class="iconfont icon-zuobiao" aria-hidden="true"></i>
                    <span>China</span>
                    <br />时间：2018-11-01——2019-05-01
                </div>
                <el-carousel height="350px">
                    <!-- 走势图 -->
                    <el-carousel-item>
                        <div id="trendChart" style="width: 400px;height:340px;"></div>
                    </el-carousel-item>
                    <!-- 饼图 -->
                    <el-carousel-item>
                        <div id="pieChart" style="width: 400px;height:340px;"></div>
                    </el-carousel-item>
                    <!-- 表格 -->
                    <el-carousel-item>
                        <div class="food-table" style="width: 400px;height:300px;">
                            <div
                                style="text-align:center;font-size:18px; color:#fff;fontWeight: bold;fontFamily: Microsoft YaHei;margin:0px 0px 10px 0px"
                            >热门话题TOP10</div>
                            <el-table
                                :data="tableData.slice((currentPage-1)*pagesize,currentPage*pagesize)"
                                :cell-style="jcRowClass"
                                :header-cell-style="jcHeadClass"
                                stripe
                                style="width: 100%;  position:absolute;"
                            >
                                <el-table-column prop="sortnum" label="排名" width="75"></el-table-column>
                                <el-table-column prop="content" label="话题" width="200"></el-table-column>
                                <el-table-column prop="hot" label="热度" width="100"></el-table-column>
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
                    </el-carousel-item>
                </el-carousel>
            </div>
        </div>
        <!-- 知识图谱关联模块 -->
        <div id="yqcompany-content" class="yqnav-content">
            <p class="modulebox_title__3Rw-h">
                <span>
                    <svg
                        style="cursor:pointer"
                        viewBox="0 0 1024 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="4023"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M976 672c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.08-0.208 0.08L512 860.048 66.784 675.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a48 48 0 0 0-36.704 88.656v0.016l463.584 191.824a1.12 1.12 0 0 0 0.208 0.08l0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 672zM29.664 348.336v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.456 47.456 0 0 0 36.672 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48.048 48.048 0 0 0 1024 304a48 48 0 0 0-29.648-44.336v-0.016L530.784 67.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a47.744 47.744 0 0 0-36.688-0.016l-0.016-0.016-0.208 0.08a1.12 1.12 0 0 1-0.208 0.08L29.648 259.648v0.016A48 48 0 0 0 0 304a48 48 0 0 0 29.664 44.336zM976 464c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.096a1.12 1.12 0 0 1-0.208 0.08L512 652.048 66.784 467.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.096-0.016 0.016a48 48 0 0 0-36.704 88.672v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 464z"
                            fill="#ffffff"
                            p-id="4024"
                        />
                    </svg>
                    <span>食品风险知识</span>
                </span>
                <span class="modulebox_hidebtn__QHdrj">
                    <svg
                        viewBox="0 0 1045 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="5501"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M282.517333 213.376l-45.354666 45.162667L489.472 512 237.162667 765.461333l45.354666 45.162667L534.613333 557.354667l252.096 253.269333 45.354667-45.162667-252.288-253.44 252.288-253.482666-45.354667-45.162667L534.613333 466.624l-252.096-253.226667z"
                            p-id="5502"
                        />
                    </svg>
                </span>
            </p>
        </div>
        <!-- 全链条关联模块 -->
        <div id="yqarea-content" class="yqnav-content">
            <p class="modulebox_title__3Rw-h">
                <span>
                    <svg
                        style="cursor:pointer"
                        viewBox="0 0 1024 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="4023"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M976 672c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.08-0.208 0.08L512 860.048 66.784 675.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a48 48 0 0 0-36.704 88.656v0.016l463.584 191.824a1.12 1.12 0 0 0 0.208 0.08l0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 672zM29.664 348.336v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.456 47.456 0 0 0 36.672 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48.048 48.048 0 0 0 1024 304a48 48 0 0 0-29.648-44.336v-0.016L530.784 67.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.08-0.016 0.016a47.744 47.744 0 0 0-36.688-0.016l-0.016-0.016-0.208 0.08a1.12 1.12 0 0 1-0.208 0.08L29.648 259.648v0.016A48 48 0 0 0 0 304a48 48 0 0 0 29.664 44.336zM976 464c-6.496 0-12.688 1.328-18.352 3.664v-0.016l-0.208 0.096a1.12 1.12 0 0 1-0.208 0.08L512 652.048 66.784 467.824a1.12 1.12 0 0 0-0.208-0.08l-0.208-0.096-0.016 0.016a48 48 0 0 0-36.704 88.672v0.016l463.584 191.824 0.208 0.08 0.208 0.08 0.016-0.016a47.6 47.6 0 0 0 36.688 0.016l0.016 0.016 0.208-0.08a1.12 1.12 0 0 1 0.208-0.08l463.568-191.824v-0.016A48 48 0 0 0 976 464z"
                            fill="#ffffff"
                            p-id="4024"
                        />
                    </svg>
                    <span>食品安全监察</span>
                </span>
                <span class="modulebox_hidebtn__QHdrj">
                    <svg
                        viewBox="0 0 1045 1024"
                        version="1.1"
                        xmlns="http://www.w3.org/2000/svg"
                        p-id="5501"
                        width="16"
                        height="16"
                    >
                        <path
                            d="M282.517333 213.376l-45.354666 45.162667L489.472 512 237.162667 765.461333l45.354666 45.162667L534.613333 557.354667l252.096 253.269333 45.354667-45.162667-252.288-253.44 252.288-253.482666-45.354667-45.162667L534.613333 466.624l-252.096-253.226667z"
                            p-id="5502"
                        />
                    </svg>
                </span>
            </p>
            <div class="food-table">
                <el-table
                    :data="SampleData.slice((currentPage-1)*pagesize,currentPage*pagesize)"
                    :cell-style="jcRowClass"
                    :header-cell-style="jcHeadClass"
                    stripe
                    style="width: 95%; position:absolute;"
                >
                    <el-table-column prop="food_name" label="食品名称" width="100"></el-table-column>
                    <el-table-column prop="num_no_pass_batch" label="不合格批次数量" width="150"></el-table-column>
                    <el-table-column prop="no_pass_rate_food" label="不合格率" width="120"></el-table-column>
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
        </div>

        <!-- 图例 -->
        <div id="legend">
            <span class="hd" style="background:rgb(255,255,255); color:rgb(0,0,0)">数量</span>
            <span class="hd" style="background:rgb(178,24,43); color:rgb(255,255,255)">1000</span>
            <span class="hd" style="background:rgb(238,114,32); color:rgb(255,255,255)">800</span>
            <span class="hd" style="background:rgb(248,187,99); color:rgb(255,255,255)">600</span>
            <span class="hd" style="background:rgb(224,218,40); color:rgb(255,255,255)">400</span>
            <span class="hd" style="background:rgb(142,173,48); color:rgb(255,255,255)">200</span>
            <span class="hd" style="background:rgba(33,102,172,0); color:rgb(255,255,255)">0</span>
        </div>
    </div>
</template>

<!-- <script type="text/javascript">
function closeContent() {
    document.getElementById("com-content").style.display = "none";
} 
</script> -->
<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
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
import echarts from "echarts";
import MapboxLanguage from "@mapbox/mapbox-gl-language";
import Nav from "@/components/Nav.vue";
import Timer from "@/components/TimeLine.vue";
import { dateFormat } from "../../static/js/formatdate.js";
import axios from "axios";
import qs from "qs";
import https from "../http.js";
export default {
    name: "Public",
    components: {
        "v-nav": Nav,
        "v-timer": Timer
    },
    data() {
        return {
            fullscreenLoading: false,
            searchVal: "",
            yqfuzzy: [],
            yqsearch: [],
            selectSearch: "",
            baseurl: "",
            layerId: "dark-v9",
            pagesize: 5,
            currentPage: 1,
            timeunit: "月",
            tableData: [
                {
                    content: "猪肉还能吃吗",
                    hot: 8.3,
                    sortnum: 1
                },
                {
                    content: "猪瘟爆发",
                    hot: 8.0,
                    sortnum: 2
                },
                {
                    content: "猪瘟爆发",
                    hot: 7.5,
                    sortnum: 3
                }
            ],
            SampleData: [
                {
                    food_name: " 牛奶",
                    no_pass_rate_food: "0.2300",
                    provinceid: "4300000000",
                    num_no_pass_batch: 345
                }
            ],
            date: "",
            options: {
                speed: 1.0, // 速度
                speedMax: 2.0 // 速度最大值
            },
            interval: 200, //日期间的间隔
            dateTimes: [],
            startTime: "",
            endTime: ""
        };
    },
    watch: {
        searchVal() {
            this.yqfocus();
            var target = document.getElementById("yq-search-scrollbar");
            if (!this.searchVal) {
                target.classList.add("closed");
            } 
        },
        selectSearch() {
            this.yqfocus();
        },
        /* startTime() {

        },
        endTime() {

        } */
    },
    mounted() {
        this.initTimeDate("2019-08-01","2019-12-01");
        this.init();
        // this.getTimeUnit(timeUnit);

        // this.fetchDefualtData(this.baseUrl, this.getParams());
    },
    methods: {
        getDateFun(time) {
            console.log("pulicsent.vue:time:" + time);
            this.date = time;
        },
        getTimeUnit(timeUnit) {
            var that = this;
            this.timeunit = timeUnit;
            if(that.startTime && that.endTime) {
                this.initTimeDate(that.startTime,that.endTime);
            } else {
                this.initTimeDate("2019-08-01","2019-12-01");
            }
            
            console.log("传到舆情页面le:" + timeUnit);
        },
        //初始化时间轴
        initTimeDate(start,end) {
            let list = [];
            var that = this;
            console.log("start:"+start+",end:"+end);
            var starttime = new Date(Date.parse(start.replace(/-/g, "/")));
            var endtime = new Date(Date.parse(end.replace(/-/g, "/")));
            function DateDiff(sDate1, sDate2) {
                //sDate1和sDate2是2006-12-18格式
                var aDate, oDate1, oDate2, iDays, iWeeks;
                aDate = sDate1.split("-");
                oDate1 = new Date(aDate[1] + "-" + aDate[2] + "-" + aDate[0]); //转换为12-18-2006格式
                aDate = sDate2.split("-");
                oDate2 = new Date(aDate[1] + "-" + aDate[2] + "-" + aDate[0]);
                iDays = parseInt(
                    Math.abs(oDate1 - oDate2) / 1000 / 60 / 60 / 24
                ); //把相差的毫秒数转换为天数
                iWeeks = parseInt(Math.ceil(iDays / 7));
                return iWeeks;
            }
            function monDateDiff(sDate1, sDate2) {
                //sDate1和sDate2是2006-12-18格式
                var aDate, oDate1, oDate2, iDays, iMonths;
                aDate = sDate1.split("-");
                oDate1 = new Date(aDate[1] + "-" + aDate[2] + "-" + aDate[0]); //转换为12-18-2006格式
                aDate = sDate2.split("-");
                oDate2 = new Date(aDate[1] + "-" + aDate[2] + "-" + aDate[0]);
                iDays = parseInt(
                    Math.abs(oDate1 - oDate2) / 1000 / 60 / 60 / 24
                ); //把相差的毫秒数转换为天数
                iMonths = parseInt(Math.ceil(iDays / 28));
                return iMonths;
            }
            var amday;
            if (that.timeunit == "周") {
                amday = DateDiff(start, endstr) + 1;
                for (let i = 0; i < amday; i++) {
                    var dateDay = starttime.getDate();
                    list.push(
                        dateFormat(starttime.toLocaleDateString(), "yyyy-MM-dd")
                    );
                    starttime.setDate(dateDay + 7);
                }
            } else {
                amday = monDateDiff(start, end);
                for (let i = 0; i < amday; i++) {
                    var dateDay = starttime.getDate();
                    list.push(
                        dateFormat(starttime.toLocaleDateString(), "yyyy-MM-dd")
                    );
                    starttime.setDate(dateDay + 28);
                }
            }
            /* var amday = monDateDiff(startstr, endstr) + 1 */
            console.log("amday:" + amday);
            console.log("starttime:" + starttime);
            that.dateTimes = list;
            that.startTime = start;
            that.endTime = end;
        },
        //分页当前所在页数
        handleCurrentChange(val) {
            this.currentPage = val;
        },
        // 表头样式设置
        jcHeadClass() {
            return "font-size:16px;text-align: center;line-height: 12px;font-weight:700;color:rgb(207, 180, 37);background-color: rgba(33,36,37,.62);";
        },
        // 表格样式设
        jcRowClass() {
            return "font-size:14px;text-align: center;line-height: 14px;";
        },
        //锁定搜索框输入
        yqfocus() {
            if (
                document.querySelector(".search-input") ==
                document.activeElement
            ) {
                this.fuzzy_search(this.searchVal.trim());
            }
        },
        //搜索框取消焦点
        yqblur() {
            //document.getElementById("search-list").classList.add("closed");
            //document.getElementById("yq-search-scrollbar").classList.add("closed");
            document.getElementById("form-inline").classList.remove("search-strength");
        },
        //模糊搜索功能
        fuzzy_search(value) {
            document.getElementById("yq-search-scrollbar").classList.remove("closed");
            var that = this;
            if (!value) {
                that.yqfuzzy = [];
                return;
            }
            let params = { keyword: this.searchVal.trim() };
            //调取模糊搜索接口
            https
                .fetchGet("/publicSent/api/getSearch", params)
                .then(response => {
                    let res = response.data;
                    this.yqfuzzy = res.message;
                    console.log("yqfuzzy:" + JSON.stringify(res));
                })
                .catch(err => {
                    console.log(err);
                });
        },
        //选中模糊匹配值
        chooseYqFuzzy(item) {
            this.searchVal = item.event_name;
            this.selectSearch = item.event_name;
            document.getElementById("search-list").classList.remove("closed");
            document.getElementById("form-inline").classList.add("search-strength");
            this.yqSearch(item.id);
        },
        //事件搜索
        yqSearch(value) {
            document.getElementById("yq-search-scrollbar").classList.add("closed");
            var that = this;
            let params = { eventId: value };
            //调取模糊搜索接口
            https
                .fetchGet("/publicSent/api/getDataset", params)
                .then(response => {
                    let res = response.data;
                    that.yqsearch = res.message;
                    console.log("yqsearch:" + JSON.stringify(res));
                })
                .catch(err => {
                    console.log(err);
                });
        },
        chooseYqSearch(value) {
            document.getElementById("search-list").classList.add("closed");
            document.getElementById("form-inline").classList.remove("search-strength");
            console.log("choosed-value:"+value.id);
            this.searchVal = this.selectSearch + ":" + value.startdate + "~" + value.enddate;
            this.startTime = value.startdate;
            this.endTime = value.enddate;
            this.initTimeDate(this.startTime,this.endTime);
           // document.getElementById("yq-search-scrollbar").classList.add("closed");
        },
        // 初始化
        init() {
            //搜索模块
            /* $(function() {
                $("input[type='search']").bind(
                    "input propertychange",
                    function() {
                        var val = $(this).val();
                        if (val === "猪肉") {
                            //搜索内容判定条件
                            document
                                .getElementById("search-list")
                                .classList.remove("closed");
                        } else {
                            document
                                .getElementById("search-list")
                                .classList.add("closed");
                        }
                    }
                );
                //获取json数据
                let dataset = getJson(
                    "../../static/data/geojson/getDataset.json"
                );
                //获取搜索结果
                
                let searchlist = document.getElementById("search-list");
                if (dataset.length > 3) {
                    //如果标签数超过3个，搜索列表变为滑动
                    searchlist.classList.add("over");
                }
                //根据json数据长度动态添加数据集，数据集内容根据自己需要设置
                for (let i = 0; i < dataset.length; i++) {
                    let li0 = document.createElement("li");
                    searchlist.appendChild(li0);
                    let a0 = document.createElement("a");
                    a0.href = "./public";
                    li0.appendChild(a0);
                    let h30 = document.createElement("h3");
                    a0.appendChild(h30);
                    let b0 = document.createElement("b");
                    b0.innerHTML = dataset[i]["event_name"];
                    h30.appendChild(b0);
                    let span0 = document.createElement("span");
                    span0.innerHTML =
                        "时间：" +
                        dataset[i]["startdate"] +
                        "——" +
                        dataset[i]["enddate"] +
                        "<br>" +
                        "地区：" +
                        dataset[i]["space"];
                    a0.appendChild(span0);
                }
            }); */

            //ajax获取json数据
            //参数：json数据url
            //返回json数据
            function getJson(url) {
                var data = [];
                $.ajax({
                    type: "GET", //请求方式
                    url: url, //地址，就是json文件的请求路径
                    async: false, //同步加载json
                    dataType: "json", //数据类型可以为 text xmljson  script  jsonp
                    success: function(result) {
                        //返回的参数就是 action里面所有的有get和set方法的参数
                        data = result.message;
                    }
                });
                return data;
            }
            //食品监察模块
            // function set_tableinspection() {
            //   let json_data = getJson(
            //     "../../static/data/geojson/getPublicOpinion.json"
            //   );
            //   let tr = $("#inspection-info tr");
            //   for (let i = 0; i < tr.length; i++) {
            //     if (i >= json_data.length) {
            //       break;
            //     }
            //     let td = $(tr[i + 1]).find("td");
            //     $(td[0]).html(json_data[i]["food_name"]);
            //     let str = Number(json_data[i]["no_pass_rate_food"] * 100).toFixed();
            //     str += "%";
            //     $(td[1]).html(str);
            //     $(td[2]).html(json_data[i]["num_no_pass_batch"]);
            //   }
            // }
            (function() {
                var NavigateBar = function(elementId) {
                    this.eId = elementId || "yq-wrap";
                    this.el = document.getElementById(this.eId);
                    this.el.addEventListener("click", function(evt) {
                        evt.stopPropagation();
                    });
                    this.state = "allClosed"; //hasOpened
                    this.currentOpenedEl = null;

                    //使用jquery就更方便使用Delegation
                    var forEach = Array.prototype.forEach;
                    var self = this;
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
                                currentEl.className = "yqnav-content";
                                //  currentEl.style.top = '0px';
                                currentEl.classList.add("yqmove_left");
                                self.state = "hasOpened";
                                self.currentOpenedEl = currentEl;
                            } else {
                                self.currentOpenedEl.className =
                                    "yqnav-content";
                                //   self.currentOpenedEl.style.top = '0px';
                                self.currentOpenedEl.classList.add(
                                    "yqmove_right"
                                );
                                currentEl.className = "yqnav-content";
                                //    currentEl.style.top = '0px';
                                currentEl.classList.add("yqmove_left");
                                self.currentOpenedEl = currentEl;
                            }
                            set_echart(
                                "../../static/data/geojson/getDefaultTrend.json"
                            );
                        });
                    });
                    var navConCloseBarList = document.querySelectorAll(
                        ".modulebox_hidebtn__QHdrj"
                    );
                    forEach.call(navConCloseBarList, function(navConCloseBar) {
                        navConCloseBar.addEventListener("click", function(evt) {
                            var currentEl =
                                evt.currentTarget.parentNode.parentNode;
                            currentEl.className = "yqnav-content";
                            //   currentEl.style.top = '0px';
                            currentEl.classList.add("yqmove_right");
                            self.state = "allClosed";
                            var yqf = document.getElementById("yqfood");
                            var yqc = document.getElementById("yqcompany");
                            var yqa = document.getElementById("yqarea");
                            yqf.classList.remove("yq-sidebar-item-active");
                            yqc.classList.remove("yq-sidebar-item-active");
                            yqa.classList.remove("yq-sidebar-item-active");
                        });
                    });
                };

                NavigateBar.prototype.close = function() {
                    this.currentOpenedEl.className = "yqnav-content";
                    //   this.currentOpenedEl.style.top = '0px';
                    this.currentOpenedEl.classList.add("yqmove_right");
                    // var currentA = document.getElementById(self.eId);
                    //  currentA.classList.remove('yq-sidebar-item-active');
                    this.state = "allClosed";
                };

                var navigateBar = new NavigateBar();
            })();

            $(".yq-sidebar-item").each(function(index) {
                $(this).click(function() {
                    $(this)
                        .addClass("yq-sidebar-item-active")
                        .siblings()
                        .removeClass("yq-sidebar-item-active");
                });
            });
            mapboxgl.accessToken =
                "pk.eyJ1IjoiY2luZHkwNzkiLCJhIjoiY2p5MW0yM2FmMDNhbzNpcnpoeGVqOXpmYSJ9.zKbdCDdA69t7b3zSWctaRw";
            const map = new mapboxgl.Map({
                container: "map", // container id
                style: "mapbox://styles/mapbox/" + this.layerId, // stylesheet location
                center: [110, 37], // starting position [lng, lat]
                zoom: 3.4 // starting zoom
            });

            var layerList = document.getElementById("menu");
            var inputs = layerList.getElementsByTagName("input");
            var _this = this; //this指的是init中的全局变量
            function switchLayer(layer) {
                var layerIdd = layer.target.id;
                _this.layerId = layerIdd;
                map.setStyle("mapbox://styles/mapbox/" + layerIdd);
                map.addControl(
                    new MapboxLanguage({
                        defaultLanguage: "zh"
                    })
                );
                _this.init();
                // new mapboxgl.Marker().setLngLat([110, 37]).addTo(map);
            }
            for (var i = 0; i < inputs.length; i++) {
                inputs[i].onclick = switchLayer;
            }

            function produce_pointJson(data) {
                var pointsJSON = {};
                var arr = [];
                data.forEach(function(row) {
                    var adcode = row["adcode"]; //获取城市代码
                    var num = row["mblog_total"]; //获取微博数，即为要生成的坐标数目
                    var pos_num = row["pos_num"];
                    var neg_num = row["neg_num"];
                    let province_code = adcode.substring(0, 2) + "0000"; //省份代码
                    var features = {};
                    var geometry = {};
                    var properties = {};
                    features.type = "Feature";
                    geometry.type = "Point";
                    properties.adcode = adcode;
                    properties.mblog_total = num;
                    properties.pos_num = pos_num;
                    properties.neg_num = neg_num;
                    features.properties = properties;
                    $.ajax({
                        type: "get", //请求方式
                        async: false,
                        url:
                            "../../static/data/geojson/provinces/" +
                            province_code +
                            ".json",
                        dataType: "json",
                        success: function(result) {
                            result = result.features;
                            result.forEach(function(e) {
                                if (
                                    e["properties"]["adcode"].toString() ===
                                    adcode
                                ) {
                                    geometry.coordinates =
                                        e["properties"]["center"];
                                    features.geometry = geometry;
                                    arr.push(features);
                                }
                            });
                        }
                    });
                });
                pointsJSON.type = "FeatureCollection";
                pointsJSON.features = arr;
                return pointsJSON;
            }

            //从json数据中匹配键值对
            //参数：需要匹配的相等的key，目标key，需要匹配的相等的value，json数组
            function match_json(mkey, aim_key, value, json_array) {
                var n = 0;
                json_array.forEach(function(row) {
                    if (row[mkey] === value) {
                        n = row[aim_key];
                    }
                });
                return n;
            }

            map.on("load", function() {
                // Add a geojson point source.
                // Heatmap layers also work with a vector tile source.
                var data = [];
                data = getJson("../../static/data/geojson/data.json");
                var sentiment = new Object(produce_pointJson(data));
                console.log(sentiment);
                map.addSource("cluster", {
                    type: "geojson",
                    data: sentiment,
                    cluster: true, // 打开聚合
                    clusterRadius: 50 // 设置聚合的半径
                    // clusterProperties: { 'Num': ["+", ["get", "mblog_total"]] } // 设置聚合过程中需要处理的数据
                });
                //添加热力图图层
                //舆论总数图层
                map.addLayer({
                    id: "Tsentiment-heat",
                    type: "heatmap",
                    source: {
                        type: "geojson",
                        data: sentiment
                    },
                    layout: {
                        visibility: "visible"
                    },
                    maxzoom: 7.5,
                    paint: {
                        "heatmap-weight": [
                            "interpolate",
                            ["linear"],
                            ["get", "mblog_total"],
                            0,
                            0,
                            1000,
                            1
                        ],

                        // Increase the heatmap color weight weight by zoom level
                        // heatmap-intensity is a multiplier on top of heatmap-weight
                        //通过缩放级别增加热图颜色重量权重
                        //热图强度是热图权重的乘法器
                        "heatmap-intensity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            3,
                            9,
                            5
                        ],
                        // Color ramp for heatmap.  Domain is 0 (low) to 1 (high).
                        // Begin color ramp at 0-stop with a 0-transparancy color
                        // to create a blur-like effect.
                        //用于热图的颜色渐变。域是0（低）到1（高）。
                        //以0透明颜色在0挡处开始颜色渐变
                        //创建模糊效果。
                        "heatmap-color": [
                            "interpolate",
                            ["linear"],
                            ["heatmap-density"],
                            0,
                            "rgba(53,181,13,0)",
                            0.2,
                            "rgb(142,173,48)",
                            0.4,
                            "rgb(224,218,40)",
                            0.6,
                            "rgb(248,187,99)",
                            0.8,
                            "rgb(238,114,32)",
                            1,
                            "rgb(178,24,43)"
                        ],
                        // Adjust the heatmap radius by zoom level
                        //通过缩放级别调整热图半径，热力图的显示半径
                        "heatmap-radius": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            2,
                            1,
                            4,
                            2,
                            8,
                            3,
                            16,
                            4,
                            32,
                            5,
                            64,
                            6,
                            128,
                            7,
                            256,
                            8,
                            512,
                            9,
                            1024,
                            10,
                            2048,
                            11,
                            4096,
                            17,
                            131072
                        ],
                        // Transition from heatmap to circle layer by zoom level
                        //变焦距转换为热图到圆图层
                        "heatmap-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            5,
                            0.95,
                            7.5,
                            0.1
                        ]
                    }
                });
                //正面数量
                map.addLayer({
                    id: "Psentiment-heat",
                    type: "heatmap",
                    source: {
                        type: "geojson",
                        data: sentiment
                    },
                    layout: {
                        visibility: "none"
                    },
                    maxzoom: 7.5,
                    paint: {
                        "heatmap-weight": [
                            "interpolate",
                            ["linear"],
                            ["get", "pos_num"],
                            0,
                            0,
                            1000,
                            1
                        ],
                        "heatmap-intensity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            3,
                            9,
                            5
                        ],
                        "heatmap-color": [
                            "interpolate",
                            ["linear"],
                            ["heatmap-density"],
                            0,
                            "rgba(53,181,13,0)",
                            0.2,
                            "rgb(142,173,48)",
                            0.4,
                            "rgb(224,218,40)",
                            0.6,
                            "rgb(248,187,99)",
                            0.8,
                            "rgb(238,114,32)",
                            1,
                            "rgb(178,24,43)"
                        ],
                        "heatmap-radius": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            2,
                            1,
                            4,
                            2,
                            8,
                            3,
                            16,
                            4,
                            32,
                            5,
                            64,
                            6,
                            128,
                            7,
                            256,
                            8,
                            512,
                            9,
                            1024,
                            10,
                            2048,
                            11,
                            4096,
                            17,
                            131072
                        ],
                        "heatmap-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            5,
                            0.95,
                            7.5,
                            0.1
                        ]
                    }
                });
                //负面热力图
                map.addLayer({
                    id: "Nsentiment-heat",
                    type: "heatmap",
                    source: {
                        type: "geojson",
                        data: sentiment
                    },
                    layout: {
                        visibility: "none"
                    },
                    maxzoom: 7.5,
                    paint: {
                        "heatmap-weight": [
                            "interpolate",
                            ["linear"],
                            ["get", "neg_num"],
                            0,
                            0,
                            1000,
                            1
                        ],

                        // Increase the heatmap color weight weight by zoom level
                        // heatmap-intensity is a multiplier on top of heatmap-weight
                        //通过缩放级别增加热图颜色重量权重
                        //热图强度是热图权重的乘法器
                        "heatmap-intensity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            3,
                            9,
                            5
                        ],
                        // Color ramp for heatmap.  Domain is 0 (low) to 1 (high).
                        // Begin color ramp at 0-stop with a 0-transparancy color
                        // to create a blur-like effect.
                        //用于热图的颜色渐变。域是0（低）到1（高）。
                        //以0透明颜色在0挡处开始颜色渐变
                        //创建模糊效果。
                        "heatmap-color": [
                            "interpolate",
                            ["linear"],
                            ["heatmap-density"],
                            0,
                            "rgba(53,181,13,0)",
                            0.2,
                            "rgb(142,173,48)",
                            0.4,
                            "rgb(224,218,40)",
                            0.6,
                            "rgb(248,187,99)",
                            0.8,
                            "rgb(238,114,32)",
                            1,
                            "rgb(178,24,43)"
                        ],
                        // Adjust the heatmap radius by zoom level
                        //通过缩放级别调整热图半径，热力图的显示半径
                        "heatmap-radius": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            0,
                            2,
                            1,
                            4,
                            2,
                            8,
                            3,
                            16,
                            4,
                            32,
                            5,
                            64,
                            6,
                            128,
                            7,
                            256,
                            8,
                            512,
                            9,
                            1024,
                            10,
                            2048,
                            11,
                            4096,
                            17,
                            131072
                        ],
                        // Transition from heatmap to circle layer by zoom level
                        //变焦距转换为热图到圆图层
                        "heatmap-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            5,
                            0.95,
                            7.5,
                            0.1
                        ]
                    }
                });

                //添加聚和图层
                //舆论总数
                map.addLayer({
                    id: "Tclusters-layer",
                    type: "circle",
                    source: "cluster",
                    minzoom: 6,
                    layout: {
                        visibility: "visible"
                    },
                    paint: {
                        "circle-radius": [
                            "step",
                            ["get", "mblog_total"],
                            20,
                            100,
                            30,
                            200,
                            40,
                            300,
                            50,
                            400,
                            60,
                            500,
                            70
                        ],
                        "circle-color": [
                            "step",
                            ["get", "mblog_total"],
                            "#51bbd6",
                            200,
                            "#f1f075",
                            300,
                            "#FFAA7F",
                            500,
                            "#f28cb1"
                        ],
                        "circle-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            6,
                            0.1,
                            9,
                            0.7
                        ]
                    }
                });
                map.addLayer({
                    id: "Tclusters-count",
                    type: "symbol",
                    source: "cluster",
                    minzoom: 6.5,
                    layout: {
                        visibility: "visible"
                    },
                    filter: [">=", ["get", "mblog_total"], 1],
                    layout: {
                        "text-field": "{mblog_total}",
                        "text-font": [
                            "DIN Offc Pro Medium",
                            "Arial Unicode MS Bold"
                        ],
                        "text-size": 20,
                        "text-allow-overlap": true
                        // 'text-optional':0.5
                    }
                });
                //正面情感
                map.addLayer({
                    id: "Pclusters-layer",
                    type: "circle",
                    source: "cluster",
                    minzoom: 6,
                    layout: {
                        visibility: "none"
                    },
                    paint: {
                        "circle-radius": [
                            "step",
                            ["get", "pos_num"],
                            20,
                            100,
                            30,
                            200,
                            40,
                            300,
                            50,
                            400,
                            60,
                            500,
                            70
                        ],
                        "circle-color": [
                            "step",
                            ["get", "pos_num"],
                            "#51bbd6",
                            200,
                            "#f1f075",
                            300,
                            "#FFAA7F",
                            500,
                            "#f28cb1"
                        ],
                        "circle-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            6,
                            0.1,
                            9,
                            0.7
                        ]
                    }
                });
                map.addLayer({
                    id: "Pclusters-count",
                    type: "symbol",
                    source: "cluster",
                    minzoom: 6.5,
                    filter: [">=", ["get", "pos_num"], 1],
                    layout: {
                        "text-field": "{pos_num}",
                        "text-font": [
                            "DIN Offc Pro Medium",
                            "Arial Unicode MS Bold"
                        ],
                        "text-size": 20,
                        "text-allow-overlap": true,
                        visibility: "none"
                    }
                });
                //负面情感
                map.addLayer({
                    id: "Nclusters-layer",
                    type: "circle",
                    source: "cluster",
                    minzoom: 6,
                    layout: {
                        visibility: "none"
                    },
                    paint: {
                        "circle-radius": [
                            "step",
                            ["get", "neg_num"],
                            20,
                            100,
                            30,
                            200,
                            40,
                            300,
                            50,
                            400,
                            60,
                            500,
                            70
                        ],
                        "circle-color": [
                            "step",
                            ["get", "neg_num"],
                            "#51bbd6",
                            200,
                            "#f1f075",
                            300,
                            "#FFAA7F",
                            500,
                            "#f28cb1"
                        ],
                        "circle-opacity": [
                            "interpolate",
                            ["linear"],
                            ["zoom"],
                            6,
                            0.1,
                            9,
                            0.7
                        ]
                    }
                });
                map.addLayer({
                    id: "Nclusters-count",
                    type: "symbol",
                    source: "cluster",
                    minzoom: 6.5,
                    filter: [">=", ["get", "neg_num"], 1],
                    layout: {
                        "text-field": "{neg_num}",
                        "text-font": [
                            "DIN Offc Pro Medium",
                            "Arial Unicode MS Bold"
                        ],
                        "text-size": 20,
                        "text-allow-overlap": true,
                        visibility: "none"
                    }
                });

                map.addSource("cities", {
                    //引入中国省份geojson数据源
                    type: "geojson",
                    data: "../../static/data/geojson/420000.json"
                });

                map.addLayer({
                    id: "points",
                    type: "symbol",
                    source: "cities",
                    layout: {
                        "text-field": "{name}",
                        "text-font": [
                            "Open Sans Semibold",
                            "Arial Unicode MS Bold"
                        ],
                        "text-offset": [0, 0.6],
                        "text-anchor": "top",
                        "text-size": 13
                    },
                    paint: {
                        "text-color": "#fff"
                    }
                });

                // map.addLayer({
                //   id: "points-hover",
                //   type: "symbol",
                //   source: "cities",
                //   layout: {
                //     "text-field": "{name}",
                //     "text-font": ["Open Sans Semibold", "Arial Unicode MS Bold"],
                //     "text-offset": [0, 0.6],
                //     "text-anchor": "top",
                //     "text-size": 13
                //   },
                //   paint: {
                //     "text-color": "#fff"
                //   },
                //   filter: [
                //     "==",
                //     "name",
                //     ""
                //   ] /* 过滤器，名字为空的数据才显示，也就是默认不使用该layer  */
                // });
            });

            //不同图层切换

            var link = document.getElementById("layer");
            var a = link.getElementsByTagName("a");
            var links = [
                ["Tsentiment-heat", "Tclusters-layer", "Tclusters-count"],
                ["Psentiment-heat", "Pclusters-layer", "Pclusters-count"],
                ["Nsentiment-heat", "Nclusters-layer", "Nclusters-count"]
            ];
            var current_id = 0;
            for (var i = 0; i < a.length; i++) {
                a[i].aaa = i;
                a[i].onclick = function(e) {
                    e.preventDefault();
                    e.stopPropagation();
                    a[current_id].className = "";
                    var visibility = map.getLayoutProperty(
                        links[this.aaa][0],
                        "visibility"
                    );
                    if (visibility !== "visible") {
                        this.className = "active";
                        for (let j = 0; j < 3; j++) {
                            map.setLayoutProperty(
                                links[this.aaa][j],
                                "visibility",
                                "visible"
                            );
                        }
                        for (let j = 0; j < 3; j++) {
                            map.setLayoutProperty(
                                links[current_id][j],
                                "visibility",
                                "none"
                            );
                        }
                        current_id = this.aaa;
                    }
                };
            }

            //悬浮窗
            var popup = new mapboxgl.Popup({
                closeButton: false,
                closeOnClick: false
            });

            map.on("mouseenter", "points", function(e) {
                var data = [];
                data = getJson("../../static/data/geojson/data.json");
                //弹出框
                // Change the cursor style as a UI indicator.
                map.getCanvas().style.cursor = "pointer";
                var province_code = e.features[0].properties.adcode.toString();
                var mblog_num = match_json(
                    "adcode",
                    "mblog_total",
                    province_code,
                    data
                );
                var pos_num = match_json(
                    "adcode",
                    "pos_num",
                    province_code,
                    data
                );
                var neg_num = match_json(
                    "adcode",
                    "neg_num",
                    province_code,
                    data
                );
                var province_name = e.features[0].properties.name;
                var coordinates = e.features[0].geometry.coordinates.slice();
                //确保弹出框位置
                while (Math.abs(e.lngLat.lng - coordinates[0]) > 180) {
                    coordinates[0] +=
                        e.lngLat.lng > coordinates[0] ? 360 : -360;
                }

                popup
                    .setLngLat(coordinates)
                    .setHTML(
                        "<strong>" +
                            province_name +
                            "</strong><br>舆论总数：" +
                            mblog_num +
                            "<br>正面情感微博数：" +
                            pos_num +
                            "<br>负面情感微博数：" +
                            neg_num
                    )
                    .addTo(map);
            });
            map.on("mouseleave", "points", function() {
                map.getCanvas().style.cursor = "";
                popup.remove();
                // map.setFilter("points-hover", ["==", "name", ""]);
            });
            //右侧弹出框弹出的具体信息
            //右侧弹出框弹出的具体信息
            map.on("click", "points", function(e) {
                var province_name = e.features[0].properties.name;
                var province_code = e.features[0].properties.adcode.toString();
                var coordinates = e.features[0].geometry.coordinates.slice();
                $("#yqfood").trigger("click");
                $("#city").text(province_name);
                $("#description span").text(
                    "经度:" +
                        Math.round(coordinates[0] * 100) / 100 +
                        "  /  纬度:" +
                        Math.round(coordinates[1] * 100) / 100
                );
            });

            // echert走势图
            var trendChart = echarts.init(
                document.getElementById("trendChart"),
                "light"
            );
            var trendoption = {
                tooltip: {
                    trigger: "axis",
                    axisPointer: {
                        // 坐标轴指示器，坐标轴触发有效
                        type: "line" // 默认为直线，可选为：'line' | 'shadow'
                    }
                },
                title: {
                    text: "微博舆论走势图",
                    left: "center",
                    textStyle: {
                        color: "#fff",
                        fontWeight: "bold",
                        fontFamily: "Microsoft YaHei"
                    }
                },
                legend: {
                    data: ["舆论总数", "正面微博数", "负面微博数"],
                    top: 25,
                    textStyle: {
                        color: "#fff",
                        fontWeight: "bold",
                        fontFamily: "Microsoft YaHei",
                        padding: [10, 0, 0, 0]
                    }
                },
                xAxis: {
                    type: "category",
                    data: [],
                    textStyle: {
                        color: "#fff",
                        fontWeight: "bold"
                    },
                    axisLine: {
                        lineStyle: {
                            color: "#fff",
                            width: "2"
                        }
                    }
                },
                yAxis: [
                    {
                        type: "value",
                        textStyle: {
                            color: "#fff",
                            fontWeight: "bold"
                        },
                        axisLine: {
                            lineStyle: {
                                color: "#fff",
                                width: "2"
                            }
                        }
                    }
                ],
                series: [
                    {
                        name: "舆论总数",
                        type: "bar",
                        stack: "舆情",
                        data: []
                    },
                    {
                        name: "正面微博数",
                        type: "bar",
                        stack: "舆情",
                        data: []
                    },
                    {
                        name: "负面微博数",
                        type: "bar",
                        stack: "舆情",
                        data: []
                    }
                ],
                color: ["#FFDB5C", "#FF704E", "#37A2DA"]
            };
            trendChart.setOption(trendoption);
            //异步加载数据
            function set_echart(url) {
                let x_date = [];
                let mblog_data = [];
                let pos_data = [];
                let neg_data = [];
                let trend_data = getJson(url);
                trend_data.forEach(function(row) {
                    x_date.push(row["startdate"].substring(5, 10));
                    mblog_data.push(row["mblog_total"]);
                    pos_data.push(row["pos_num"]);
                    neg_data.push(row["neg_num"]);
                });

                trendChart.setOption({
                    xAxis: {
                        data: x_date
                    },
                    series: [
                        {
                            name: "舆论总数",
                            data: mblog_data
                        },
                        {
                            name: "正面微博数",
                            data: pos_data
                        },
                        {
                            name: "负面微博数",
                            data: neg_data
                        }
                    ]
                });
            }
            // set_echart();

            // echert饼图
            // echert饼图
            var pieChart = echarts.init(
                document.getElementById("pieChart"),
                "light"
            );
            var pieoption = {
                title: {
                    text: "情感分析图",
                    left: "center",
                    textStyle: {
                        color: "#fff",
                        fontWeight: "bold",
                        fontFamily: "Microsoft YaHei"
                    }
                },
                legend: {
                    orient: "vertical",
                    top: 50,
                    left: "left",
                    textStyle: {
                        color: "#fff",
                        fontFamily: "Microsoft YaHei"
                    },
                    data: ["正面情感微博数", "负面情感微博数"]
                },
                series: [
                    {
                        name: "情感分析",
                        type: "pie",
                        radius: "55%",
                        center: ["50%", "60%"],
                        label: {
                            normal: {
                                formatter: "{b} :" + "\r\n" + "{c} ({d}%)",
                                position: "inside",
                                fontSize: 13
                            }
                        },
                        data: [
                            { value: 335, name: "正面情感微博数" },
                            { value: 700, name: "负面情感微博数" }
                        ]
                    }
                ],
                color: ["#FF704E", "#37A2DA"]
            };
            pieChart.setOption(pieoption);

            //话题热度Top10
            function set_tabledata() {
                let topic_data = getJson(
                    "../../static/data/geojson/getTopic.json"
                );
                let tr = $("#topicTop tr");
                for (let i = 0; i < tr.length; i++) {
                    if (i >= topic_data.length) {
                        break;
                    }
                    let td = $(tr[i + 1]).find("td");
                    $(td[0]).html(topic_data[i]["sortnum"]);
                    $(td[1]).html(topic_data[i]["content"]);
                    $(td[2]).html(topic_data[i]["hot"]);
                }
            }
            //弹出框关闭按钮
            /* let closeBar = document.querySelector("div.yq-close");
      closeBar.addEventListener("click", function(evt) {
        var currentEl = evt.currentTarget.parentNode;
        currentEl.className = "yqmove_right";
        setTimeout(function() {
          currentEl.classList.add("closed");
        }, 1000);
      }); */

            //   const language = new MapboxLanguage({ defaultLanguage: "zh" });
            // map.addControl(language);
            map.addControl(
                new MapboxLanguage({
                    defaultLanguage: "zh"
                })
            );

            map.addControl(new mapboxgl.NavigationControl());
        }
    },
    computed: {}
};
</script>


