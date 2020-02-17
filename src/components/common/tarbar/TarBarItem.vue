<template>
  <div class="tar-bar-item" @click="activeBar">
    <div v-if="!isActive">
      <slot name="tar-icon"></slot>
    </div>
    <div v-else>
      <slot name="tar-icon-active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="tar-text"></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: "TarBarItem",
    data(){
      return {
        //isActive:false
      }
    },
    props:{
      path:String,
      activeColor:{
        type:String,
        default:'#ff5777'
      }
    },
    methods:{
      activeBar(){
        this.$router.replace(this.path)
      }
    },
    computed:{
      isActive(){
        return this.$route.path.indexOf(this.path)!==-1
      },
      activeStyle(){
        return this.isActive?{color:this.activeColor}:''
      }
    }
  }
</script>

<style scoped>
  .tar-bar-item{
    flex: 1;
    text-align: center;
  }
  .tar-bar-item img{
    width: 24px;
    height: 24px;
  }
</style>
