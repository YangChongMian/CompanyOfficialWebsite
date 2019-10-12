<template>
    <div id="app">
        <PageTitle class="page-title" :message="message"/>
        <div class="container">
            <div class="lefts">
                <ImgAndFont v-for="(item,index) in news" :class="index == 1 ? 'iaf' :''" :key="index" :news="item"/>
            </div>
            <div class="rights">
                <div class="titles">
                    <div class="icons"></div>
                    <span>京弘达咨询</span>
                </div>
                <img class="img-style" v-for="(item,index) in imgList" :src="item" alt="" :key="index"/>
            </div>
        </div>
    </div>
</template>
<script>
    import ImgAndFont from './childComponents/imgAndFont.vue'
    import PageTitle from './childComponents/pageTitle.vue'
    export default {
        components:{
            PageTitle,
            ImgAndFont,
        },
        data: function () {
            return {
                message:{
                    chs:'新闻中心',
                    enss:'Recruitment'
                },
                imgList:[
                    require('./../assets/imgs/index/news4.png'),
                    require('./../assets/imgs/index/news5.png'),
                    require('./../assets/imgs/index/news6.png'),
                    require('./../assets/imgs/index/news7.png'),
                ],
                news:[
                    {
                        src:require('./../assets/imgs/index/news1.png'),
                        type:'实时资讯',
                        title:'卫健委正式发文！绩效怎么考核？试管百万医护人员~',
                        contents:'通过绩效考核保障三级公立医院的健康、持续发展，一直是医 改重要议程，为全面推进三级公立医院绩效考核工作，确保绩 效考核数据客观真实可比，国家卫健委发布了《关于启动2019 年全国三级公立医院绩效考核有关工作的通知》（以下简称《 通知》），对考核的相关工作做出了要求。具体如下...',
                        date:'京弘达信息技术有限公司 日期：2019-5-6'
                    },
                    {
                        src:require('./../assets/imgs/index/news2.png'),
                        type:'实时资讯',
                        title:'卫健委正式发文！绩效怎么考核？试管百万医护人员~',
                        contents:'通过绩效考核保障三级公立医院的健康、持续发展，一直是医 改重要议程，为全面推进三级公立医院绩效考核工作，确保绩 效考核数据客观真实可比，国家卫健委发布了《关于启动2019 年全国三级公立医院绩效考核有关工作的通知》（以下简称《 通知》），对考核的相关工作做出了要求。具体如下...',
                        date:'京弘达信息技术有限公司 日期：2019-5-6'
                    },
                    {
                        src:require('./../assets/imgs/index/news3.png'),
                        type:'实时资讯',
                        title:'卫健委正式发文！绩效怎么考核？试管百万医护人员~',
                        contents:'通过绩效考核保障三级公立医院的健康、持续发展，一直是医 改重要议程，为全面推进三级公立医院绩效考核工作，确保绩 效考核数据客观真实可比，国家卫健委发布了《关于启动2019 年全国三级公立医院绩效考核有关工作的通知》（以下简称《 通知》），对考核的相关工作做出了要求。具体如下...',
                        date:'京弘达信息技术有限公司 日期：2019-5-6'
                    }
                ]
            }
        },
        created: function () {


        },
        methods: {}
    }
</script>
<style scoped>
    .page-title{
        margin:40px auto;
    }
    .container{
        width:1200px;
        margin:0 auto;
        display:flex;
        justify-content: space-between;
    }
    .rights{
        width:300px;
        display: flex;
        flex-direction:column;
        justify-content:space-around;
    }
    .titles{
        display:flex;
    }
    .icons{
        width:4px;
        height:22px;
        background-color: #0066a2;
        margin-right:5px;
    }
    .img-style{
        border:1px solid transparent;
    }
    .img-style:hover{
        border:1px solid #0066a2;
        transition:all linear 0.5s;
    }
    .iaf{
        margin:40px 0;
    }
</style>
