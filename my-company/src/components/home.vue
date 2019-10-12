<template>
    <div id="app">
        <div class="bgi">
            <div class="banners">
                <img src="./../assets/imgs/index/topContainerFont.png" alt=""/>
                <div class="banner-six">
                    <ul>
                        <li class="banner-hover" v-for="(item,index) in banners" :key="index" :style="index%2 == 1 ? bannerBgi  : ''">
                            <h2>{{item.titles}}</h2>
                            <p>{{item.middles}}</p>
                            <p>{{item.enTitles}}</p>
                            <img v-if="index%2 == 1" src="./../assets/imgs/index/iconWhite.png" alt=""/>
                            <img v-else src="./../assets/imgs/index/iconblue.png" alt=""/>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data: function () {
            return {
                bannerBgi:{
                    'background':'#5799ce',
                    'color':'#fff'
                },
                banners:[
                    {titles:'医院管理信息导航',bgi:'',middles:'',enTitles:'Hospital Management Information Navigation'},
                    {titles:'医院医用耗材数据分析系统',bgi:'url("./../assets/imgs/index/banner1.png")',middles:'',enTitles:'Hospital Medical Consumables Data Analysis System'},
                    {titles:'医院医用耗材精细化管理系统',bgi:'',middles:'（三合一解决方案）',enTitles:'Fine Management System of Medical Consumablesin Hospital (Trinity Solution)'},
                    {titles:'医院绩效管理系统',middles:'',bgi:'url("./../assets/imgs/index/banner2.png")',enTitles:'Hospital Performance Management System'},
                    {titles:'智慧就医引导服务',middles:'',bgi:'',enTitles:'Intelligent Medical Guidance Service'},
                    {titles:'医院运营统计服务系统',middles:'',bgi:'url("./../assets/imgs/index/banner3.png")',enTitles:'Hospital Operation Statistics Service System'},
                ]
            }
        },
        created: function () {


        },
        methods: {}
    }
</script>
<style scoped>
    #app{
        margin-top:100px;
        position:relative;
    }
    .bgi{
        width:100%;
        height:655px;
        background-image: url('./../assets/imgs/index/topContainerBg.png');
        -webkit-background-size: 100% 100%;
        background-size: 100% 100%;
        background-repeat: no-repeat;
        margin-bottom: 250px;
    }
    .banners{
        width:1200px;
        height:655px;
        margin:0 auto;
        position:relative;
    }
    .banner-hover:hover{
        transition:all ease-in 0.08s;
        font-size:17px;
    }
    .banner-hover{
        position:relative;
    }
    .banner-hover>img{
        position:absolute;
        bottom:20px;
    }
    .banners>img{
        position:absolute;
        right:0;
        top:160px;
    }
    .banner-six{
        width:1200px;
        position:absolute;
        bottom:-194px;
        background-color: #fff;
        color:#5799ce;
    }
    ul{
        display:flex;
        flex-wrap:wrap;
    }
    li{
        width:400px;
        height:194px;
        text-align:center;
        padding:70px 0;
    }
</style>
