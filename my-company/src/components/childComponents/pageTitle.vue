<template>
    <div id="title">
        <div class="ch">{{ message.chs }}</div>
        <div class="en">{{ message.enss }}</div>
    </div>
</template>
<script>
    export default {
        props:['message']
    }
</script>
<style scoped>
    #title{
        width:240px;
        height:80px;
    }
    .ch{
        font-size:36px;
        color:#2a85c6;
    }
    .en{
        font-size:24px;
        color:#2a85c6;
    }
</style>
