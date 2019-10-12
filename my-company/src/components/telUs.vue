<template>
    <div id="telUs">
        <PageTitle class="page-title" :message="message"/>
        <div class="container">
            <div class="list-parent">
                <ul class="lists">
                    <li v-for="(item,index) in list" :key="index">{{ item }}</li>
                </ul>
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
                    chs:'联系我们',
                    enss:'Contact Us'
                },
                list:[
                    '邮箱： jinghongda_beijing@jinghongda.net',
                    'Tel  ： 010-53512827',
                    '传真： 010-58851337',
                    '地址： 北京海淀区复兴路83号玉兴商务楼206室',
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
        width:100%;
        padding:50px 0;
        background-color: #ccc;
    }
    .list-parent{
        width:100%;
        background-color: #888888;
    }
    .lists{
        width:480px;
        margin:0 auto;
        text-align: left;
        padding:20px;
    }
    li{
        height:60px;
        font-size:20px;
        color:#fff;
        display: flex;
        align-items:center;
    }
</style>
