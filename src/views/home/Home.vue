<template>
  <div id="home">
    <nav-bar class="nav-bar-center">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
    <recommend-views :recommends="recommends"></recommend-views>
    <feature-view></feature-view>
  </div>
</template>

<script>
  import NavBar from 'components/common/navbar/NavBar'
  import HomeSwiper from './childComps/HomeSwiper'
  import RecommendViews from './childComps/RecommendViews'
  import FeatureView from './childComps/FeatureView'

  import {getHomeMultidata} from "network/home";

  export default {
    name: "Home",
    data(){
      return {
        banners:[],
        recommends:[]
      }
    },
    components:{
      NavBar,
      HomeSwiper,
      RecommendViews,
      FeatureView
    },
    created() {
      getHomeMultidata()
        .then(res=>{
          // console.log(res)
          this.banners = res.data.banner.list
          this.recommends = res.data.recommend.list
        })
    }
  }
</script>

<style scoped>
.nav-bar-center{
  background-color: var(--color-tint);
  color: #ffffff;
  position: fixed;
  right: 0px;
  left: 0px;
  top: 0px;
  z-index: 10;
}
  #home{
    padding-top: 44px;
  }
</style>
