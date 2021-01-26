<template>
  <div class="nav-bar">
    <div class="left" @click="goback"><slot name="left"><img src="~assets/images/left.png"></slot></div>
    <div class="center"><slot></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script>
import {useRouter} from 'vue-router'
export default {
    setup(){
        const router = useRouter();
        const goback = () => {
            router.go(-1);
        }

        return {
            goback
        }
    }
}
</script>

<style lang="less" scoped>
.nav-bar {
  background-color: var(--color-tint);
  color: #fff;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 9;
  height: 45px;
  line-height: 45px;
  text-align: center;
  box-shadow: 0 2px 0px rgba(100, 100, 100, 0.1);
  display: flex;
  .left,
  .right {
    width: 60px;
  }
  .center {
    flex: 1;
  }
  img{
  width: 24px;
  height: 24px;
  font-size: 12px;
  line-height: 24px;

  }
}
</style>
