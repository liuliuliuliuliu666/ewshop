<template>
  <div>
   <nav-bar>
        <template v-slot:left></template>
        <template v-slot>购物车</template>
        <template v-slot:right></template>
    </nav-bar>
  </div>
</template>

<style lang="less" scoped>

</style>

<script>
import NavBar from 'components/common/navbar/NavBar'
export default {
    components: {
        NavBar
    }
}
</script>