<template>
  <div class="tar-bar">
    <slot></slot>
  </div>
</template>

<script>
  import TarBarItem from './TarBarItem'
  export default {
    name: "TarBar",
    components:{
      TarBarItem
    }
  }
</script>

<style scoped>
  .tar-bar{
    display: flex;
    height: 49px;
    background-color: #f7f7f7;
    box-shadow: 1px -1px 1px rgba(0,0,0,0.09);
    position: fixed;
    left: 0px;
    right: 0px;
    bottom: 0px;
  }


</style>
