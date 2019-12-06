<template>
  <div id="app">
    <div class="foot">
      <router-link tag="span" to="/home">首页</router-link>
      <router-link tag="span" to="/my">我的</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
.foot{
   display: flex;
   justify-content: space-around;
   background: #f0f0f0;
   height: 40px;
   line-height: 40px;
   position: fixed;
   width: 100%;
   left: 0;
   bottom: 0;
   span.router-link-active{
     color:lightblue
   }
}
</style>
