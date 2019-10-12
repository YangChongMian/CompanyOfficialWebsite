<template>
    <div id="app">
        <div class="containers">
            <div class="tow-content">
                <div class="fonts">
                    <PageTitle class="page-title" :message="message"/>
                    <p class="fonts-content" v-for="(fonts,index) in fonts" :key="index"> &nbsp; &nbsp; &nbsp; &nbsp;{{ fonts }}</p>
                </div>
                <div class="leftImg">
                    <img src="./../assets/imgs/index/buildings.png" alt=""/>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import PageTitle from './childComponents/pageTitle.vue'
    export default {
        components:{
            PageTitle,
        },
        data: function () {
            return {
                message:{
                    chs:'公司简介',
                    enss:'Company Profile'
                },
                fonts:[
                    '京弘达信息技术(北京)有限公司是国内医疗数据应用管理的领导者，荟萃了医院信息管理专 家、医院标准化管理专家、大数据行业专家和医学临床专家等多个体系的顶尖专业人员并研 发出我国首个基于数据超级汇总的医用耗材检测与管理系统和医疗价格服务监督与管理系统。',
                    '京弘达信息技术(北京)有限公司与国内顶级医院保持长期紧密产学研合作关系，公司凭借一 流的行业人才队伍，发挥在现代管理、统计学、计算机信息化等方面的技术优势，推出了一 系列医疗改革下的信息化通用产品；在海量医疗数据挖掘、数据应用管理、多维多向信息可 视化、医学信息安全和隐私保护技术等方面累积了坚实的技术基础和丰富的项目实践经验； 使公司建立起具前瞻性的行业应用方案，也建立完整的数据应用体系。',
                    '本着“数据服务医疗，创新缔造价值”的宗旨，京弘达将先进的管理理念和卓越的技术以咨询 设计、数据服务的方式为国家、军队、地方政府、医疗机构提供一站式信息化的监测与管理 服务；助力患者降低就医成本、助力医院提高医疗管理效率、助力政府优化医保管控方式。'
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
        width:100%;
        height:546px;
        text-align: left;
        display: flex;
        align-items:center;
        margin-top:10px;
    }
    .page-title{
        margin:40px 0;
    }
    .containers{
        width:100%;
        height:500px;
        background-color: #ccc;
    }
    .tow-content{
        width:1200px;
        margin:0 auto;
        font-size:20px;
        position:relative;
    }
    .fonts{
        width:660px;
        height:500px;
        float:right;
    }
    .fonts>.fonts-content{
        font-size:14px;
        line-height:24px;
    }
    .leftImg{
        position:absolute;
        top:-23px;
    }
</style>
