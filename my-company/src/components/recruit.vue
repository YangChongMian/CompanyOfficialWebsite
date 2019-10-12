<template>
    <div id="recruit">
        <Recruit class="pageTitle" :message="titles"/>
        <div class="pages">
            <div>
                <a>了解职位详情>></a>
            </div>
        </div>
    </div>
</template>
<script>
    import Recruit from './childComponents/pageTitle.vue'
    export default {
        components:{
            Recruit,
        },
        data: function () {
            return {
                titles:{
                    chs:'人才招聘',
                    enss:'Recruitment'
                }
            }
        },
        created: function () {


        },
        methods: {}
    }
</script>
<style scoped>
    .pageTitle{
        margin:40px auto;
    }
    .pages{
        width:100%;
        height:544px;
        background-image: url('./../assets/imgs/index/recBgImg.png');
        -webkit-background-size: 100% 100%;
        background-size: 100% 100%;
        background-repeat: no-repeat;
        position:relative;
    }
    .pages>div{
        width: 260px;
        height: 140px;
        padding: 44px 40px;
        background-color: rgba(0,0,0,0.35);
        position: absolute;
        right: 150px;
        bottom: 80px;
    }
    .pages>div>a{
        display: inline-block;
        width: 180px;
        height: 52px;
        line-height: 52px;
        text-align: center;
        border-radius: 10px;
        border: 1px solid #fff;
        color: #fff;
        cursor: pointer;
    }
    .pages>div>a:hover{
        color:#0066a2;
        border:1px solid #00
    }
</style>
