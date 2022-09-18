<template>
<popup/>
<headers/>
<content/>
<footers :data="data.footer"/>
</template>

<script>
import data from '../api/商品数据.js';
import '@/assets/iconfont.js';
import headers from '@/components/header'
import content from '@/components/Content'
import footers from '@/components/footer'
import popup from '@/components/popup.vue'
export default {
    components:{
        headers,content, footers,popup
    },
    setup(){
        return {data}
    }
}
</script>

<style>
html,body,h1,h2,h3,h4,h5,h6,div,ul,ol,li,dl,dt,dd,iframe,textarea,input,button,p,strong,b,a,span,del,pre,figure,figcaption{margin:0; padding:0; -webkit-text-size-adjust:none;}
h1,h2,h3,h4,h5,h6,em,del{font-style:normal; font-weight:normal; font-size:100%; -webkit-text-size-adjust:none;}

ul,dl,ol{list-style:none;}
img{border:0;}
html,body{height:100%;}
html,body{font-size:14px; font-family:Microsoft YaHei, Tahoma, Geneva, sans-serif; width: 100%; height: 100%;}
a{text-decoration:none;color:#000}
</style>
