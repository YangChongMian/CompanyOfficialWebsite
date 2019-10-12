<template>
  <div id="app">
    <div class="topnav" id="topnav">
      <TopNav/>
    </div>
    <div class="homes" id="homes">
      <Home/>
    </div>
    <div class="profile" id="profile">
      <Profile/>
    </div>
    <div class="lunbo" id="lunbo">
      <Lunbo/>
    </div>
    <div class="news" id="news">
      <New/>
    </div>
    <div class="recruit" id="recruit">
      <Recruit/>
    </div>
    <div class="ourCustomer" id="ourCustomer">
      <OurCustomer/>
    </div>
    <div class="telUs" id="telUs">
      <TelUs/>
    </div>
    <div class="footer">
      COPYRIGHT BY @2011 JINGHONGDA CO.,LTD. ALL RIGHT RESERVED 京弘达信息技术(北京)有限公司
    </div>
  </div>
</template>

<script>
import TopNav from './components/topnav.vue';
import Home from './components/home.vue';
import Profile from './components/profile.vue';
import Lunbo from './components/lunbo.vue';
import New from './components/news.vue';
import Recruit from './components/recruit.vue';
import OurCustomer from './components/ourCustomer.vue';
import TelUs from './components/telUs.vue';
export default {
  name: 'app',
  components: {
    TopNav,
    Home,
    Profile,
    Lunbo,
    New,
    Recruit,
    OurCustomer,
    TelUs,
  },
  mounted:function(){

  },
  methods:{

  }
}
</script>

<style>
  *{
    padding:0;
    margin:0;
    list-style: none;
    box-sizing: border-box;
  }
  html::-webkit-scrollbar{
    display:none;
  }
  html{
    transition:all linear 0.2s;
  }
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .topnav{
    display: flex;
  }
  .footer{
    height: 90px;
    background-color: rgba(72,72,72,0.4);
    line-height: 90px;
    text-align: center;
    color: #fff;
    margin-top:40px;
  }
</style>
