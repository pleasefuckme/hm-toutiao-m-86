<template>
  <div class="container">

<!--    <van-nav-bar-->
<!--      title="工单系统"-->
<!--      left-text="返回"-->
<!--      right-text="按钮"-->
<!--      left-arrow-->
<!--      @click-left="onClickLeft"-->
<!--      @click-right="onClickRight"-->
<!--    />-->
<!--     顶部导航 -->
    <van-nav-bar v-if="showNavbar" fixed title="工单系统" right-text="搜索" @click-right="$router.push('/search')" />
<!--     内容容器 -->
    <div class="my-wrapper" :class="{noTop:!showNavbar}">
      <!-- 二级路由对应组件显示容器 -->
      <router-view></router-view>
    </div>
    <!-- 底部tab栏 -->
    <van-tabbar route>
      <van-tabbar-item to="/" icon="home-o">工单</van-tabbar-item>
      <van-tabbar-item to="/question" icon="chat-o">消息</van-tabbar-item>
      <van-tabbar-item to="/video" icon="video-o">我的</van-tabbar-item>
      <van-tabbar-item to="/user" icon="user-o">我的</van-tabbar-item>
    </van-tabbar>

<!--    <van-tabbar v-model="active">-->
<!--      <van-tabbar-item icon="home-o">标签</van-tabbar-item>-->
<!--      <van-tabbar-item icon="search" dot>标签</van-tabbar-item>-->
<!--      <van-tabbar-item icon="friends-o" info="5">标签</van-tabbar-item>-->
<!--      <van-tabbar-item icon="setting-o" info="20">标签</van-tabbar-item>-->
<!--    </van-tabbar>-->
  </div>
</template>

<script>
export default {
  computed: {
    // 判断是否显示头部导航
    showNavbar () {
      return this.$route.path !== '/user'
    }
  }
}
</script>

<style scoped lang='less'>
.container{
  width: 100%;
  height: 100%;
  position: relative;
  .my-wrapper{
    width: 100%;
    height: 100%;
    overflow: hidden;
    padding-top: 46px;
    padding-bottom: 50px;
    box-sizing: border-box;
    &.noTop{
      padding-top: 0;
    }
  }
}
</style>
