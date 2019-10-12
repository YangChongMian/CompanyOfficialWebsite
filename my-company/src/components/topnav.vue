<template>
    <div id="app">
        <div class="containers">
            <div class="logo">
                <img src="./../assets/imgs/index/logo.png" alt=""/>
            </div>
            <ul>
                <li :class="menuActive == index  ? 'active' : ''  " v-for="(item,index) in menuList" :key="item">
                    <a @click="clickItem(index)">{{ item }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
    export default {
        data: function () {
            return {
                menuList:['首页','公司简介','公司产品','案例分析','新闻中心','人才招聘','我们的客户','联系我们'],
                menuActive:0,
                pageHeight:[]
            }
        },
        created: function () {

        },
        mounted:function(){
            this.getH();
            window.addEventListener('scroll',this.windowScroll,true);
        },
        methods: {
            windowScroll:function(){
                let scrollHeight = window.pageYOffset || document.documentElement.clientHeight || document.body.clientHeight;
                if(scrollHeight > this.pageHeight[0]){
                    this.menuActive = 0;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200){
                    this.menuActive = 1;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]){
                    this.menuActive = 1;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]+this.pageHeight[3]){
                    this.menuActive = 3;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]+this.pageHeight[3]+this.pageHeight[4]){
                    this.menuActive = 4;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]+this.pageHeight[3]+this.pageHeight[4]+this.pageHeight[5]){
                    this.menuActive = 5;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]+this.pageHeight[3]+this.pageHeight[4]+this.pageHeight[5]+this.pageHeight[6]){
                    this.menuActive = 6;
                }
                if(scrollHeight > this.pageHeight[0]+this.pageHeight[1]-200+this.pageHeight[2]+this.pageHeight[3]+this.pageHeight[4]+this.pageHeight[5]+this.pageHeight[6]+this.pageHeight[7]){
                    this.menuActive = 7;
                }
            },
            getH:function(){
                let h1 = 0;
                let h2 = document.getElementById('homes').clientHeight+200+40;
                let h3 = 0;
                let h4 = document.getElementById('profile').clientHeight;
                let h5 = document.getElementById('lunbo').clientHeight+40;
                let h6 = document.getElementById('news').clientHeight+80;
                let h7 = document.getElementById('recruit').clientHeight+20;
                let h8 = document.getElementById('ourCustomer').clientHeight;
                this.pageHeight.push(h1,h2,h3,h4,h5,h6,h7,h8);
            },
            clickItem:function(index){
                this.menuActive = index;
                let scrollTop = 0;
                if(index != 2){
                    this.pageHeight.map((item,indexs) => {
                        if(indexs <= index){
                            scrollTop += item;
                        }
                    });
                    document.documentElement.scrollTop = scrollTop;
                }
            }
        }
    }
</script>
<style scoped>
#app{
    width:100%;
    box-shadow:2px 2px 10px #ccc;
    position:fixed;
    top:0;
    z-index:1;
    background-color: #fff;
}
.containers{
    width:1200px;
    height:100px;
    margin:0 auto;
    display: flex;
    align-items:center;
}
.logo>img{
    width:90%;
}
ul{
    margin-left:50px;
    display: flex;
    height:100px;
}
li{
    width:125px;
    height:100px;
    align-items:center;
    display: flex;
    justify-content: center;
    border-bottom:2px solid transparent;
    transition:all linear 0.1s;
}
.active{
    border-bottom:2px solid #0066a2;
}
a{
    cursor:pointer;
}
</style>
