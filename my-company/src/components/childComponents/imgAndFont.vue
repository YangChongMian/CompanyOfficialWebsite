<template>
    <div id="imgAndFont">
        <img class="imgs" :src="news.src" alt=""/>
        <div class="right-font">
            <p class="types">{{ news.type }}</p>
            <p class="title">{{ news.title }}</p>
            <p class="contents">{{ news.contents }}</p>
            <p class="date">{{ news.date }}</p>
        </div>
    </div>
</template>
<script>
    export default {
        props:['news'],
        data: function () {
            return {}
        },
        created: function () {


        },
        methods: {}
    }
</script>
<style scoped>
    #imgAndFont{
        width:860px;
        height:228px;
        background-color: #fff;
        display:flex;
        text-align: left;
        align-items:center;
        box-sizing: border-box;
        padding:10px 0 10px 10px;
    }
    #imgAndFont:hover{
        background-color: #cccccc;
    }
    .imgs{
        width:295px;
        height:187px;
    }
    .right-font{
        width:500px;
        height:187px;
        margin-left:22px;
    }
    .types{
        font-size:14px;
        color:#0066a2;
    }
    .title{
        font-size:18px;
        color:#0b0b0b;
        margin-bottom:25px;
    }
    .contents{
        width:500px;
        height:90px;
        color:#757a81;
        font-size:12px;
    }
    .date{
        color:#757a81;
        font-size:12px;
    }
</style>
