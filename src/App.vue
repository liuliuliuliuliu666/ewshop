<template>
  <div id="nav">
    <router-link to="/home" class="tab-bar-item">
    <div class="icon"><i class="iconfont icon-shouye-01"></i></div>
    <div>首页</div>
    </router-link> 
    <router-link to="/category" class="tab-bar-item">
    <div class="icon"><i class="iconfont icon-biaoqiankuozhan_fenlei-127"></i></div>
    <div>分类</div>
    </router-link>
    <router-link to="/shopCart" class="tab-bar-item">
    <div class="icon"><i class="iconfont icon-gouwuche"></i></div>
    <div>购物车</div>
    </router-link>
    <router-link to="/profile" class="tab-bar-item">
    <div class="icon"><i class="iconfont icon-yiliaohangyedeICON-"></i></div>
    <div>我的</div>
    </router-link>
  </div>
  <router-view/>
</template>

<style lang="less">
@import url('assets/css/base.css');
@import url('assets/css/iconfont.css');
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  background-color: #f6f6f6;
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: 0 -10px 1px rgba(100,100,100,.1);
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: var(--color-high-text);
    }
  }
  .tab-bar-item{
  flex: 1;
  text-align: center;
  height: 50px;
  font-size: 12px;
  .icon{
  width: 24px;
  height: 24px;
  display: inline-block;
  vertical-align: middle;
  margin-top: 5px;
  }
  }
}
</style>
