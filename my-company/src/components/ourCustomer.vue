<template>
    <div id="ourCustomer">
        <PageTitle class="page-title" :message="message"/>
        <ul>
            <li class="list" v-for="(item,index) in customerList">
                <span :class="index == 0 ? 'first' : 'other' "></span>
                <span>{{ item }}</span>
            </li>
        </ul>
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
                    chs:'我们的客户',
                    enss:'our Clients'
                },
                customerList:[
                    '第一医学中心 (原301医院本部）',
                    '第二医学中心（原301南楼临床部）',
                    '第三医学中心（原武警总医院）',
                    '第四医学中心（原304医院）',
                    '第五医学中心（原302及307医院）',
                    '第六医学中心（原海军总医院）',
                    '第七医学中心（原陆军总医院）',
                    '第八医学中心（原309医院）',
                    '陆军第八十集团军医院',
                    '海南医院（原海南分院）',
                    '上海长海医院',
                    '宁波市妇女儿童医院',
                    '· · · · · ·',
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
    .first{
        display: inline-block;
        width:30px;
        height:30px;
        background-image: url('./../assets/imgs/index/listStyle1.png');
        -webkit-background-size: 100% 100%;
        background-size: 100% 100%;
        margin-right:12px;
    }
    .other{
        display: inline-block;
        width:30px;
        height:30px;
        background-image: url('./../assets/imgs/index/listStyle.png');
        -webkit-background-size: 100% 100%;
        background-size: 100% 100%;
        margin-right:12px;
    }
    ul{
        width:870px;
        margin:0 auto;
        display: flex;
        flex-wrap:wrap;
        padding-left:70px;
    }
    .list{
        width:400px;
        display: flex;
        height:80px;
        align-items:center;
    }
    span{
        font-size:20px;
    }
</style>
