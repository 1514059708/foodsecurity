<template>
    <div id="knowledge">
        <!-- 插件导航 -->
        <div id="mynetwork"></div>
        <!-- Navigation -->
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

        <!-- 可收缩列表 
        <div id="mySidebar" class="sidebar" onmouseover="toggleSidebar()" onmouseout="toggleSidebar()"></div>-->

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
        </div>

        <div id="zsfood-content" class="zsnav-content">
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
            <!-- <div class="zsnav-con-close">
                <i class="glyphicon glyphicon-chevron-right"></i>
            </div>-->
            <div class="zs-zl">
                <el-carousel height="340px">
                    <el-carousel-item v-for="item in zhishidata" :key="item.食品ID">
                        <div class="zhishisave">
                            <p>
                                <span class="food-card-title">{{item.食品名称}}</span>
                                <span class="food-card-subtitle">又名:{{item.食品别名}}</span>
                                <span class="food-card-icon" style="color:rgb(100,190,230)">
                                    <i class="fa fa-th-large" aria-hidden="true"></i>
                                    食品类别：
                                </span>
                                <span class="food-card-item">{{item.食品类别}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(245,200,55)">
                                    <i class="fa fa-leaf" aria-hidden="true"></i>
                                    添加剂名称：
                                </span>

                                <span class="food-card-item">{{item.添加剂名称}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(255,85,65)">
                                    <i class="fa fa-bomb" aria-hidden="true"></i>
                                    产生危害：
                                </span>
                                <span class="food-card-item">{{item.产生危害.危害详情}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(120,215,175)">
                                    <i class="fa fa-cutlery" aria-hidden="true"></i>
                                    添加作用：
                                </span>
                                <span class="food-card-item">{{item.添加作用.作用详情}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(255,242,198)">
                                    <i class="fa fa-pencil-square-o" aria-hidden="true"></i>
                                    鉴别方法：
                                </span>
                                <span class="food-card-item">{{item.鉴别方法}}</span>
                                <br />
                            </p>
                        </div>
                    </el-carousel-item>
                </el-carousel>
            </div>
        </div>
        <div id="zscompany-content" class="zsnav-content">
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
                    <span>食品安全事件</span>
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
            <!-- <div class="zsnav-con-close">
                <i class="glyphicon glyphicon-chevron-right"></i>
            </div>-->
            <div class="zs-zl">
                <el-carousel height="340px">
                    <el-carousel-item v-for="item in caseitem" :key="item.id">
                        <div class="zhishisave">
                            <!-- <div v-html="item"></div> -->
                            <p>
                                <span class="food-card-title">{{item.event_name}}</span>
                                <span class="food-card-subtitle">爆发时间:{{item.startdate}}</span>
                                <span class="food-card-icon" style="color:rgb(100,190,230)">
                                    <i
                                        class="fa fa-map-marker"
                                        aria-hidden="true"
                                        style="font-size: 16px;width: 12px;text-align: center;"
                                    ></i>
                                    发生地点：
                                </span>
                                <span class="food-card-item">{{item.address}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(245,200,55)">
                                    <i class="fa fa-bullseye" aria-hidden="true"></i>
                                    受灾程度：
                                </span>

                                <span class="food-card-item">{{item.degree}}</span>
                                <br />
                                <span class="food-card-icon" style="color:rgb(255,85,65)">
                                    <i class="fa fa-info-circle" aria-hidden="true"></i>
                                    具体情况：
                                </span>
                                <span class="food-card-item">{{item.caption}}</span>

                                <br />
                            </p>

                            <!-- <p>{{item.txth}}</p>
                            <p v-html="item.txt"></p>-->
                        </div>
                    </el-carousel-item>
                </el-carousel>
            </div>
        </div>
        <div id="zsarea-content" class="zsnav-content">
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
            <!-- <div class="zsnav-con-close">
                <i class="glyphicon glyphicon-chevron-right"></i>
            </div>-->
            <div class="zs-zl">
                <!-- <div class="zs-img"><img src="../../static/image/timg.jpg"></div> -->
                <div id="myChartChina" :style="{width: '150px', height: '300px'}"></div>
            </div>
        </div>

        <div class="left-zs">
            <div id="zscd" class="left-size">
                <p>知识词典</p>
                <el-tree :data="treedata" :props="defaultProps" @node-click="handleNodeClick"></el-tree>
            </div>
        </div>
    </div>
</template>

<script src="https://unpkg.com/vis-network/standalone/umd/vis-network.min.js"></script>
<script src="../../static/js/vis-network.min.js"></script>
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
import Nav from "@/components/Nav.vue";
import vis from "vis";
export default {
    name: "Knowledge",
    components: {
        "v-nav": Nav
    },
    data() {
        return {
            search: "",
            searchData: "",
            products: [
                //假数据
                { name: "数据1", date: "2018-01-04", depart: "泸化工1" },
                { name: "数据2", date: "2018-01-25", depart: "泸化工2" },
                { name: "数据3", date: "2018-02-10", depart: "泸化工3" },
                { name: "数据4", date: "2018-03-04", depart: "泸化工4" },
                { name: "数据5", date: "2018-05-24", depart: "泸化工5" },
                { name: "数据6", date: "2018-10-29", depart: "泸化工6" }
            ],

            caseitem: [
                {
                    id: 1,
                    event_name: "非洲猪瘟",
                    startdate: "2018-08-03",
                    address: "沈阳市",
                    degree: "中等",
                    caption:
                        "发病猪场383家，猪发病数量47头，死亡数量47头，OIE公布死亡和扑杀数量28783头，解除封锁时间2018年9月29日零时"
                },
                {
                    id: 2,
                    event_name: "非洲猪瘟",
                    startdate: "2018-10-03",
                    address: "黄冈市",
                    degree: "中等",
                    caption:
                        "发病猪场383家，猪发病数量47头，死亡数量47头，OIE公布死亡和扑杀数量28783头，解除封锁时间2018年9月29日零时"
                },
                {
                    id: 3,
                    event_name: "非洲猪瘟",
                    startdate: "2018-09-30",
                    address: "营口市",
                    degree: "严重",
                    caption:
                        "发病猪场378家，猪发病数量102头，死亡数量102头，OIE公布死亡和扑杀数量46643头，解除封锁时间2018年11月22日零时"
                }
            ],
            zhishidata: [
                {
                    食品ID: "F003001",
                    食品名称: "红壳瓜子",
                    食品别名: "天葵子,望日葵子,向日葵子,葵瓜子,毛嗑,西瓜子",
                    食品类别: "休闲食品",
                    添加剂编号: "T0047",
                    添加剂名称: "酸性橙",
                    产生危害: {
                        危害编号: "7",
                        危害等级: "3",
                        危害详情: "致癌"
                    },
                    添加作用: { 作用编号: "5", 作用详情: "着色" },
                    鉴别方法: "色泽自然才是好的,吃红瓜子的时候别用嘴接触瓜子皮"
                },
                {
                    食品ID: "F003002",
                    食品名称: "瓜子",
                    食品别名: "天葵子,望日葵子,向日葵子,葵瓜子,毛嗑,西瓜子",
                    食品类别: "休闲食品",
                    添加剂编号: "T8848",
                    添加剂名称: "山梨酸钾",
                    产生危害: {
                        危害编号: "2",
                        危害等级: "1",
                        危害详情: "无"
                    },
                    添加作用: { 作用编号: "8", 作用详情: "防腐" },
                    鉴别方法: "暂无"
                },
                {
                    食品ID: "F003003",
                    食品名称: "天葵子",
                    食品别名: "天葵子,望日葵子,向日葵子,葵瓜子,毛嗑,西瓜子",
                    食品类别: "休闲食品",
                    添加剂编号: "T8848",
                    添加剂名称: "山梨酸钾",
                    产生危害: {
                        危害编号: "2",
                        危害等级: "1",
                        危害详情: "无"
                    },
                    添加作用: { 作用编号: "8", 作用详情: "防腐" },
                    鉴别方法: "暂无"
                }
            ],
            treedata: [
                {
                    id: 1,
                    label: "猪肉类",
                    children: [
                        {
                            id: 5,
                            label: "猪肉",
                            children: [
                                {
                                    id: 10,
                                    label: "猪腿肉"
                                },
                                {
                                    id: 11,
                                    label: "猪血"
                                }
                            ]
                        }
                    ]
                },
                {
                    id: 2,
                    label: "苹果",
                    children: [
                        {
                            id: 6,
                            label: "苹果派"
                        },
                        {
                            id: 7,
                            label: "苹果汁"
                        }
                    ]
                },
                {
                    id: 3,
                    label: "牛奶",
                    children: [
                        {
                            id: 8,
                            label: "乳酪"
                        },
                        {
                            id: 9,
                            label: "酸奶"
                        }
                    ]
                },
                {
                    id: 4,
                    label: "牛肉",
                    children: [
                        {
                            id: 10,
                            label: "牛排"
                        },
                        {
                            id: 11,
                            label: "牛蒡"
                        }
                    ]
                }
            ],
            defaultProps: {
                children: "children",
                label: "label"
            }
        };
    },
    mounted() {
        this.init();
    },
    methods: {
        getFoodName() {
            this.$http.get("../../static/data/foodcircle.json").then(
                response => {
                    console.log(
                        "response:" +
                            JSON.stringify(response.data.data.nodelist)
                    );
                },
                response => {
                    alert("服务器请求失败");
                }
            );
        },
        init() {
            this.getFoodName();
            (function() {
                var NavigateBar = function(elementId) {
                    this.eId = elementId || "zs-wrap";
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
                                currentEl.className = "zsnav-content";
                                //  currentEl.style.top = '0px';
                                currentEl.classList.add("zsmove_left");
                                console.log(
                                    "diyici开始之前的evt.currentTarget.id:" +
                                        evt.currentTarget.id
                                );
                                self.state = "hasOpened";
                                self.currentOpenedEl = currentEl;
                            } else {
                                self.currentOpenedEl.className =
                                    "zsnav-content";
                                //   self.currentOpenedEl.style.top = '0px';
                                self.currentOpenedEl.classList.add(
                                    "zsmove_right"
                                );
                                currentEl.className = "zsnav-content";
                                //    currentEl.style.top = '0px';
                                currentEl.classList.add("zsmove_left");
                                self.currentOpenedEl = currentEl;
                            }
                        });
                    });

                    var navConCloseBarList = document.querySelectorAll(
                        ".modulebox_hidebtn__QHdrj"
                    );
                    console.log("有效果吗");
                    forEach.call(navConCloseBarList, function(navConCloseBar) {
                        navConCloseBar.addEventListener("click", function(evt) {
                            var currentEl =
                                evt.currentTarget.parentNode.parentNode;

                            currentEl.className = "zsnav-content";
                            //   currentEl.style.top = '0px';
                            currentEl.classList.add("zsmove_right");
                            self.state = "allClosed";
                            var zsf = document.getElementById("zsfood");
                            var zsc = document.getElementById("zscompany");
                            var zsa = document.getElementById("zsarea");
                            zsf.classList.remove("zs-sidebar-item-active");
                            zsc.classList.remove("zs-sidebar-item-active");
                            zsa.classList.remove("zs-sidebar-item-active");
                            console.log(self, evt);
                            console.log("nihao");
                        });
                    });
                };

                NavigateBar.prototype.close = function() {
                    this.currentOpenedEl.className = "zsnav-content";
                    //   this.currentOpenedEl.style.top = '0px';
                    this.currentOpenedEl.classList.add("zsmove_right");
                    // var currentA = document.getElementById(self.eId);
                    //  currentA.classList.remove('zs-sidebar-item-active');
                    console.log("this.currentOpenedEl:" + this.currentOpenedEl);
                    this.state = "allClosed";
                };

                var navigateBar = new NavigateBar();
            })();

            $(".zs-sidebar-item").each(function(index) {
                $(this).click(function() {
                    $(this)
                        .addClass("zs-sidebar-item-active")
                        .siblings()
                        .removeClass("zs-sidebar-item-active");
                });
            });

            var nodes = new vis.DataSet([
                { id: 1, label: "猪肉", group: "F" },
                { id: 2, label: "盐酸克伦特罗", group: "A" },
                { id: 3, label: "中毒", group: "D" },
                { id: 4, label: "头晕", group: "D" },
                { id: 5, label: "恶心", group: "D" },
                { id: 6, label: "心跳加速", group: "D" },
                { id: 7, label: "昏迷", group: "D" },
                { id: 8, label: "致死", group: "D" },
                { id: 9, label: "致癌", group: "D" },
                { id: 10, label: "莱克多巴胺", group: "A" },
                { id: 11, label: "硝基呋喃类药物", group: "A" },
                { id: 12, label: "致畸", group: "D" },
                { id: 13, label: "禽肉", group: "F" },
                { id: 14, label: "动物性水产", group: "F" },
                { id: 15, label: "抗生素残渣", group: "A" },
                { id: 16, label: "过敏", group: "D" },
                { id: 17, label: "荨麻疹", group: "D" },
                { id: 18, label: "耐药性变强", group: "D" },
                { id: 19, label: "瘦肉精", group: "F" },
                { id: 20, label: "镇静剂", group: "A" },
                { id: 21, label: "呕吐", group: "D" },
                { id: 22, label: "呼吸困难", group: "D" },
                { id: 23, label: "牛羊肉及肝脏", group: "F" },
                { id: 24, label: "抗感染", group: "E" },
                { id: 25, label: "提高瘦肉率", group: "E" },
                { id: 26, label: "镇静", group: "E" },
                { id: 27, label: "催眠", group: "E" },
                { id: 28, label: "减少能耗", group: "E" },
                { id: 29, group: "M", label: "鉴别方法" },
                { id: 30, group: "M", label: "鉴别方法" },
                { id: 32, group: "M", label: "鉴别方法" },
                { id: 33, group: "M", label: "鉴别方法" },
                { id: 34, group: "M", label: "鉴别方法" }
                //*******************************************************************************************************最后两个参数：X为画布长，y分别为：
                //{id: 35, label: '食品',group:'F',fixed: {x:true,y:true},x:800,y:560},                                     //画布高-240
                //{id: 36, label: '添加剂',group:'A',fixed: {x:true,y:true},x:800,y:620},                                   //画布高-180
                //{id: 37, label: '鉴别方法',group:'M',fixed: {x:true,y:true},x:800,y:680},                                 //画布高-120
                //{id: 38, label: '人体危害',group:'D',fixed: {x:true,y:true},x:800,y:730},                                 //画布高-70
                //{id: 39, label: '添加作用',group:'E',fixed: {x:true,y:true},x:800,y:800},                                 //画布高
                //*****************************************************************************************************
            ]);

            // 定义关系
            var edges = new vis.DataSet([
                { from: 2, to: 1, arrows: "to", title: "添加到" },
                { from: 1, to: 3, arrows: "to", title: "一次摄入过多下产生" },
                { from: 2, to: 3, arrows: "to", title: "一次摄入过多下产生" },
                { from: 1, to: 4, arrows: "to", title: "一次摄入过多下产生" },
                { from: 2, to: 5, arrows: "to", title: "一次摄入过多下产生" },
                { from: 1, to: 6, arrows: "to", title: "一次摄入过多下产生" },
                { from: 2, to: 6, arrows: "to", title: "一次摄入过多下产生" },
                { from: 1, to: 7, arrows: "to", title: "一次摄入过多下产生" },
                { from: 2, to: 7, arrows: "to", title: "一次摄入过多下产生" },
                { from: 1, to: 8, arrows: "to", title: "一次摄入过多下产生" },
                { from: 2, to: 8, arrows: "to", title: "一次摄入过多下产生" },
                { from: 1, to: 9, arrows: "to", title: "长期食用下产生" },
                { from: 2, to: 9, arrows: "to", title: "长期食用下产生" },
                { from: 10, to: 1, arrows: "to", title: "添加到" },
                { from: 10, to: 3, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 4, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 5, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 6, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 7, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 8, arrows: "to", title: "一次摄入过多下产生" },
                { from: 10, to: 9, arrows: "to", title: "长期食用下产生" },
                { from: 11, to: 1, arrows: "to", title: "添加到" },
                { from: 1, to: 9, arrows: "to", title: "产生" },
                { from: 11, to: 9, arrows: "to", title: "产生" },
                { from: 1, to: 12, arrows: "to", title: "产生" },
                { from: 11, to: 12, arrows: "to", title: "产生" },
                { from: 11, to: 13, arrows: "to", title: "添加到" },
                { from: 13, to: 9, arrows: "to", title: "产生" },
                { from: 13, to: 12, arrows: "to", title: "产生" },
                { from: 11, to: 14, arrows: "to", title: "添加到" },
                { from: 14, to: 9, arrows: "to", title: "产生" },
                { from: 14, to: 12, arrows: "to", title: "产生" },
                { from: 15, to: 1, arrows: "to", title: "添加到" },
                { from: 1, to: 16, arrows: "to", title: "微量食用下产生" },
                { from: 15, to: 16, arrows: "to", title: "微量食用下产生" },
                { from: 1, to: 17, arrows: "to", title: "微量食用下产生" },
                { from: 15, to: 17, arrows: "to", title: "微量食用下产生" },
                { from: 1, to: 18, arrows: "to", title: "微量食用下产生" },
                { from: 15, to: 18, arrows: "to", title: "微量食用下产生" },
                { from: 19, to: 1, arrows: "to", title: "添加到" },
                { from: 19, to: 3, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 4, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 5, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 6, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 7, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 8, arrows: "to", title: "一次摄入过多下产生" },
                { from: 19, to: 9, arrows: "to", title: "长期食用下产生" },
                { from: 20, to: 1, arrows: "to", title: "添加到" },
                { from: 20, to: 21, arrows: "to", title: "产生" },
                { from: 1, to: 21, arrows: "to", title: "产生" },
                { from: 20, to: 22, arrows: "to", title: "产生" },
                { from: 1, to: 22, arrows: "to", title: "产生" },
                { from: 20, to: 5, arrows: "to", title: "产生" },
                { from: 20, to: 6, arrows: "to", title: "产生" },
                { from: 19, to: 23, arrows: "to", title: "添加到" },
                { from: 23, to: 3, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 4, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 5, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 6, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 7, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 8, arrows: "to", title: "一次摄入过多下产生" },
                { from: 23, to: 9, arrows: "to", title: "长期食用下产生" },
                { from: 15, to: 24, arrows: "to", title: "目的" },
                { from: 1, to: 24, arrows: "to", title: "目的" },
                { from: 10, to: 25, arrows: "to", title: "目的" },
                { from: 1, to: 25, arrows: "to", title: "目的" },
                { from: 23, to: 25, arrows: "to", title: "目的" },
                { from: 19, to: 25, arrows: "to", title: "目的" },
                { from: 14, to: 24, arrows: "to", title: "目的" },
                { from: 13, to: 24, arrows: "to", title: "目的" },
                { from: 2, to: 25, arrows: "to", title: "目的" },
                { from: 1, to: 26, arrows: "to", title: "目的" },
                { from: 20, to: 26, arrows: "to", title: "目的" },
                { from: 1, to: 27, arrows: "to", title: "目的" },
                { from: 20, to: 27, arrows: "to", title: "目的" },
                { from: 1, to: 28, arrows: "to", title: "目的" },
                { from: 20, to: 28, arrows: "to", title: "目的" },
                { from: 1, to: 29, arrows: "to", title: "鉴别方法" },
                { from: 15, to: 29, arrows: "to", title: "鉴别方法" },
                { from: 1, to: 30, arrows: "to", title: "鉴别方法" },
                { from: 10, to: 30, arrows: "to", title: "鉴别方法" },
                { from: 23, to: 31, arrows: "to", title: "鉴别方法" },
                { from: 19, to: 31, arrows: "to", title: "鉴别方法" },
                { from: 19, to: 32, arrows: "to", title: "鉴别方法" },
                { from: 1, to: 32, arrows: "to", title: "鉴别方法" },
                { from: 1, to: 33, arrows: "to", title: "鉴别方法" },
                { from: 11, to: 33, arrows: "to", title: "鉴别方法" },
                { from: 13, to: 33, arrows: "to", title: "鉴别方法" },
                { from: 14, to: 33, arrows: "to", title: "鉴别方法" },
                { from: 2, to: 32, arrows: "to", title: "鉴别方法" },
                { from: 1, to: 34, arrows: "to", title: "鉴别方法" },
                { from: 20, to: 34, arrows: "to", title: "鉴别方法" }
            ]);

            //创建网络
            var container = document.getElementById("mynetwork");
            var data = {
                nodes: nodes,
                edges: edges
            };
            //配置
            var options = {
                locale: "cn",
                //configure: {
                //  enabled: true,
                //  filter: 'physics',
                //  container: undefined,
                //  showButton: true},    //不可以自己调节物理参数
                autoResize: true, //开启自动调整
                height: "100%",
                width: "100%",
                clickToUse: true, //开启鼠标事件
                edges: { length: 200 },
                groups: {
                    F: {
                        color: "#FFCC33",
                        shape: "image",
                        image: "static/image/f.png",
                        font: { size: 23, color: "#FFE4B5" },
                        title: "食品"
                    }, //食品，字体加大
                    A: {
                        color: "#FA8072",
                        shape: "image",
                        image: "static/image/a.png",
                        title: "添加剂",
                        font: { size: 16.5, color: "#FFA07A" }
                    }, //添加剂
                    M: {
                        color: "#48D1CC",
                        shape: "image",
                        image: "static/image/m.png",
                        title: "鉴别方法",
                        font: { size: 16.5, color: "#E1FFFF" }
                    }, //鉴别方法
                    D: {
                        color: "#FFC0CB",
                        shape: "image",
                        image: "static/image/d.png",
                        title: "人体危害",
                        font: { size: 16.5, color: "#FAFAD2" }
                    }, //人体危害
                    E: {
                        color: "#87CEFA",
                        shape: "image",
                        image: "static/image/e.png",
                        title: "添加作用",
                        font: { size: 16.5, color: "#7FFFAA" }
                    } //添加作用
                },
                edges: {
                    to: {
                        color: { color: "#F5F5F5", inherit: "from" },
                        arrows: {
                            scaleFactor: 1,
                            imageHeight: 15,
                            imageWidth: 15,
                            type: "bar"
                        }
                    },
                    middle: {
                        color: { color: "#F5F5F5", inherit: "from" },
                        arrows: {
                            scaleFactor: 1,
                            imageHeight: 15,
                            imageWidth: 15,
                            type: "bar"
                        }
                    },
                    from: {
                        color: { color: "#F5F5F5", inherit: "from" },
                        arrows: {
                            scaleFactor: 1,
                            imageHeight: 15,
                            imageWidth: 15,
                            type: "bar"
                        }
                    }
                }
            };

            var network = new vis.Network(container, data, options);
            var myChartContainer = document.getElementById("myChartChina");
            var resizeMyChartContainer = function() {
                myChartContainer.style.width =
                    document.body.offsetWidth / 3.5 + "px"; //页面一半的大小
            };
            resizeMyChartContainer();
            var myChartChina = this.$echarts.init(myChartContainer);

            function randomData() {
                return Math.round(Math.random() * 500);
            }
            // 绘制图表
            var optionMap = {
                tooltip: {},
                legend: {
                    orient: "vertical",
                    left: "left",
                    data: [""]
                },
                visualMap: {
                    min: 0,
                    max: 1500,
                    top: "bottom",
                    calculable: true,
                    color: ["black", "#2d4e7a"]
                },
                selectedMode: "single",
                series: [
                    {
                        name: "感染数量：",
                        numb: "",
                        type: "map",
                        mapType: "china",
                        itemStyle: {
                            normal: {
                                borderColor: "rgb(167, 164, 164)"
                            },
                            emphasis: {
                                shadowOffsetX: 0,
                                shadowOffsetY: 0,
                                shadowBlur: 20,
                                borderWidth: 0,
                                shadowColor: "rgba(0, 0, 0, 0.5)"
                            }
                        },
                        showLegendSymbol: true,
                        label: {
                            normal: {
                                show: false
                            },
                            emphasis: {
                                show: true
                            }
                        },
                        data: [
                            { name: "北京", value: randomData() },
                            { name: "天津", value: randomData() },
                            { name: "上海", value: randomData() },
                            { name: "重庆", value: randomData() },
                            { name: "河北", value: randomData() },
                            { name: "河南", value: randomData() },
                            { name: "云南", value: randomData() },
                            { name: "辽宁", value: randomData() },
                            { name: "黑龙江", value: randomData() },
                            { name: "湖南", value: randomData() },
                            { name: "安徽", value: randomData() },
                            { name: "山东", value: randomData() },
                            { name: "新疆", value: randomData() },
                            { name: "江苏", value: randomData() },
                            { name: "浙江", value: randomData() },
                            { name: "江西", value: randomData() },
                            { name: "湖北", value: randomData() },
                            { name: "广西", value: randomData() },
                            { name: "甘肃", value: randomData() },
                            { name: "山西", value: randomData() },
                            { name: "内蒙古", value: randomData() },
                            { name: "陕西", value: randomData() },
                            { name: "吉林", value: randomData() },
                            { name: "福建", value: randomData() },
                            { name: "贵州", value: randomData() },
                            { name: "广东", value: randomData() },
                            { name: "青海", value: randomData() },
                            { name: "西藏", value: randomData() },
                            { name: "四川", value: randomData() },
                            { name: "宁夏", value: randomData() },
                            { name: "海南", value: randomData() },
                            { name: "台湾", value: randomData() },
                            { name: "香港", value: randomData() },
                            { name: "澳门", value: randomData() }
                        ]
                    }
                ]
            };

            myChartChina.setOption(optionMap);
            window.onresize = function() {
                resizeMyChartContainer();
                myChartChina.resize();
            };
        },
        handleNodeClick(data) {
            console.log(data);
        }
    }
};
</script>

<style>
@import "../../static/css/bootstrap.css";
@import "../../static/css/bootstrap.min.css";
@import "../../static/css/animate.css";
@import "../../static/css/style.css";
@import "../../static/css/zstp.css";
@import "../../static/css/jcfx.css";
@import "../../static/css/pe-icons.css";
@import "../../static/css/font-awesome-4.1.0/css/font-awesome.min.css";
#knowledge {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background: #343332;
}
@-webkit-keyframes zsmove_right {
    from {
        opacity: 1;
    }
    to {
        opacity: 0;
        -webkit-transform: translateX(540px);
        transform: translateX(540px);
    }
}

@keyframes zsmove_right {
    from {
        opacity: 1;
    }
    to {
        opacity: 0;
        -webkit-transform: translateX(540px);
        transform: translateX(540px);
    }
}

@-webkit-keyframes zsmove_left {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
        -webkit-transform: translateX(-540px);
        transform: translateX(-540px);
    }
}

@keyframes zsmove_left {
    from {
        opacity: 0;
    }
    to {
        opacity: 1;
        -webkit-transform: translateX(-540px);
        transform: translateX(-540px);
    }
}
.zsmove_right {
    -webkit-animation-name: zsmove_right;
    animation-name: zsmove_right;
    -webkit-animation-duration: 1.4s;
    animation-duration: 1.4s;
    -webkit-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    transition-timing-function: linear;
}

.zsmove_left {
    -webkit-animation-name: zsmove_left;
    animation-name: zsmove_left;
    -webkit-animation-duration: 1.4s;
    animation-duration: 1.4s;
    -webkit-animation-iteration-count: 1;
    animation-iteration-count: 1;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    transition-timing-function: linear;
}
/* 走马灯的左右切换  */
.el-carousel--horizontal {
    margin-top: 0 !important;
}
.el-carousel__arrow {
    background-color: rgba(250, 250, 249, 0.5) !important;
}
.el-carousel__item h3 {
  color: #ccc;
  font-size: 14px;
  opacity: 0.75;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  color: #fff;
  border: 1px solid rgb(255, 212, 3);
  background-color: rgba(47,50,51,.78);
  box-shadow: 0px 35px 77px -17px rgba(0,0,0,0.44);
}

.el-carousel__item:nth-child(2n+1) {
  color: #fff;
  border: 1px solid rgb(255, 212, 3);
  box-shadow: 0px 35px 77px -17px rgba(0,0,0,0.44);
  background-color: transparent;
 /* background-color: rgba(47,50,51,.78); */
}
</style>
