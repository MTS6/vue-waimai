<template>
  <div class="footer-guide">
    <span class="guide-item " :class="{on: $route.path === '/msite'}" @click="goto('/msite')">
      <span>
        <i class="iconfont icon-u"></i>
      </span>
        <span>首页</span>
    </span>
    <span class="guide-item" :class="{on: $route.path === '/search'}" @click="goto('/search')">
      <span>
        <i class="iconfont icon-search1"></i>
      </span>
        <span>搜索</span>
    </span>
    <span class="guide-item" :class="{on: $route.path === '/order'}" @click="goto('/order')">
      <span>
        <i class="iconfont icon-dingdan3"></i>
      </span>
        <span>订单</span>
    </span>
    <span class="guide-item" :class="{on: $route.path === '/profile'}" @click="goto('/profile')">
      <span>
        <i class="iconfont icon-user"></i>
      </span>
        <span>我的</span>
    </span>
  </div>
</template>
<script tyrpe="text/ecmascript-6">
export default {

  methods: {
    goto(url){
      this.$router.replace(url)
    }
  },
}
</script>

<style scoped lang="stylus" rel="stylesheet/stylus">
@import '../../common/stylus/mixins.styl'
  .footer-guide
    top-border-1px(#cccccc)
    position fixed
    display flex
    left 0
    bottom 0
    height 50px
    width 100%
    .guide-item
      display flex
      flex-direction column
      width 25%
      text-align center
      &.on
        color $green
      span
        margin-top 3px
        font-size 12px
        i 
          font-size 22px
          
</style>