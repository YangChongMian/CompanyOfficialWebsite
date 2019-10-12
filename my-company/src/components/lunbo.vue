<template>
    <div id="lunbo">
        <PageTitle class="page-title" :message="message"/>
        <div class="lunbo-content">
            <div class="arrow">
                <img @click="clickL" src="./../assets/imgs/index/swipLeft.png" alt=""/>
            </div>
            <div class="middle-content">
                <div class="image-content" :style="contentStyle">
                    <ImgWithinDiv :imgs="images1"/>
                    <ImgWithinDiv :imgs="images2"/>
                </div>
            </div>
            <div class="arrow">
                <img @click="clickR" src="./../assets/imgs/index/swipRight.png" alt=""/>
            </div>
        </div>
        <ul class="point">
            <li v-for="item in 2"></li>
        </ul>

    </div>
</template>
<script>
    import PageTitle from './childComponents/pageTitle.vue'
    import ImgWithinDiv from './childComponents/imgWithinDiv.vue'
    export default {
        components:{
            PageTitle,
            ImgWithinDiv,
        },
        data: function () {
            return {
                images1:[require('./../assets/imgs/index/swipper1.png'),require('./../assets/imgs/index/swipper2.png'),require('./../assets/imgs/index/swipper3.png')],
                images2:[require('./../assets/imgs/index/swipper1.png'),require('./../assets/imgs/index/swipper3.png'),require('./../assets/imgs/index/swipper2.png')],
                contentStyle:{
                    left:0,
                    transition:'all ease-in 0.5s'
                },
                count:0,
                message:{
                    chs:'案例分析',
                    enss:'Case Analysis'
                },
            }
        },
        created: function () {

        },
        methods: {
            clickL:function(){
                this.count--;
                if(this.count > -1){
                    this.contentStyle.left = this.count*1053+'px';
                }else{
                    this.contentStyle.left = -1053+'px';
                    this.count = 1;
                }
            },
            clickR:function(){
                this.count++;
                if(this.count < 2){
                    this.contentStyle.left = -this.count*1053+'px';
                }else{
                    this.contentStyle.left = 0;
                    this.count = 0;
                }
            }
        }
    }
</script>
<style scoped>
    #lunbo{
        margin:20px 0;
    }
    .page-title{
        width:100%;
        margin:40px auto;
    }
    .lunbo-content{
        display: flex;
        align-items:center;
        justify-content:center;
        position:relative;
    }
    .middle-content{
        width:1053px;
        height:266px;
        overflow: hidden;
        position:relative;
        display: flex;
    }
    .image-content{
        display: flex;
        position:absolute;
    }
    .arrow{
        margin:0 10px;
    }
    .point{
        width:100%;
        display: flex;
        justify-content:center;
    }
    ul.point>li{
        width:10px;
        height:10px;
        background-color: #0066a2;
        border-radius:50%;
        margin:10px;
    }
</style>
