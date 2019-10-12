<template>
    <div id="imgWithinDiv">
        <div>
            <div class="imgs" v-for="(item,index) in imgs" :key="index" :style="{backgroundImage:'url('+item+')'}">
                <img :src="item" alt=""/>
                {{ item }}
            </div>
            <!--<div>-->
                <!--<img src="./../../assets/imgs/index/swipper2.png" alt=""/>-->
            <!--</div>-->
            <!--<div>-->
                <!--<img src="./../../assets/imgs/index/swipper3.png" alt=""/>-->
            <!--</div>-->
        </div>
    </div>
</template>
<script>
    export default {
        props:['imgs'],
        data: function () {
            return {

            }
        },
        created: function () {


        },
        methods: {}
    }
</script>
<style scoped>
    #imgWithinDiv{
        width:1053px;
        height:270px;
    }
    #imgWithinDiv>div{
        display: flex;
    }
    .imgs{
        width:341px;
        height:266px;
        margin:0 5px;
    }
</style>
