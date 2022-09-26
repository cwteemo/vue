<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"/>
    <recommend-view :recommends="banners"/>
  </div>
</template>

<script>
import NavBar from "@/components/common/navbar/NavBar";
import HomeSwiper from "@/views/home/childHome/HomeSwiper";
import RecommendView from "@/views/home/childHome/RecommendView";
import {getHomeMultiData} from "@/network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
    RecommendView
  },
  data(){
    return {
      banners: [
        {
          title:'图片一',
          link:'',
          image:'http://192.168.1.105/jiagong/public/index.php/file/url?token=816kT6nYnf3834rPq8718Gbm20&name=uploads%2F2%2F37%2F48%2Fedit%2Ffceb3c440308a7ebcc79356bcf1f979a.png',
        },
        {
          title:'图片二',
          link:'',
          image:'http://192.168.1.105/jiagong/public/index.php/file/url?token=816kT6nYnf3834rPq8718Gbm20&name=uploads%2F2%2F37%2F48%2F97d9b2ff8e42bacc5f99cbea053fa6ac.png',
        },
        {
          title:'图片三',
          link:'',
          image:'http://192.168.1.105/jiagong/public/index.php/file/url?token=816kT6nYnf3834rPq8718Gbm20&name=uploads%2F2%2F37%2F48%2Ff5a5f5cb0061493f4737a5dfcca54d08.png',
        },
        {
          title:'图片四',
          link:'',
          image:'http://192.168.1.105/jiagong/public/index.php/file/url?token=816kT6nYnf3834rPq8718Gbm20&name=uploads%2F2%2F37%2F48%2Fab509d2de1f9d94c925d8d60b244ec2c.png',
        },
        {
          title:'图片五',
          link:'',
          image:'http://192.168.1.105/jiagong/public/index.php/file/url?token=816kT6nYnf3834rPq8718Gbm20&name=uploads%2F2%2F37%2F48%2Ff27e2ce587d4f4ae701a785c50a1f076.png',
        },
      ],
      recommends: [],
    }
  },
  created() {
    getHomeMultiData().then(res=>{
      console.log(res);
    })
  },
  methods: {
    aa() {
      console.log(this.$router)
    }
  }
}
</script>

<style scoped>
  .home-nav {
    background-color: var(--color-tint);
    color: #f6f6f6;
  }
</style>
