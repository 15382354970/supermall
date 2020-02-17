<template>
  <div>
    <tar-bar>
      <tar-bar-item path="home">
        <img slot="tar-icon" src="../../assets/img/tabbar/home.svg" alt="">
        <img slot="tar-icon-active" src="../../assets/img/tabbar/home_active.svg" alt="">
        <div slot="tar-text">首页</div>
      </tar-bar-item>
      <tar-bar-item path="category">
        <img slot="tar-icon" src="../../assets/img/tabbar/category.svg" alt="">
        <img slot="tar-icon-active" src="../../assets/img/tabbar/category_active.svg" alt="">
        <div slot="tar-text">分类</div>
      </tar-bar-item>
      <tar-bar-item path="cart">
        <img slot="tar-icon" src="../../assets/img/tabbar/cart.svg" alt="">
        <img slot="tar-icon-active" src="../../assets/img/tabbar/cart_active.svg" alt="">
        <div slot="tar-text">购物车</div>
      </tar-bar-item>
      <tar-bar-item path="profile">
        <img slot="tar-icon" src="../../assets/img/tabbar/profile.svg" alt="">
        <img slot="tar-icon-active" src="../../assets/img/tabbar/profile_active.svg" alt="">
        <div slot="tar-text">我的</div>
      </tar-bar-item>
    </tar-bar>
  </div>
</template>

<script>
  import TarBar from '../common/tarbar/TarBar'
  import TarBarItem from '../common/tarbar/TarBarItem'
  export default {
    name: "MainTarBar",
    components:{
      TarBar,
      TarBarItem
    }
  }
</script>

<style scoped>

</style>
