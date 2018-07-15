<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <!-- 页面跳转，to指的是页面跳转的路径 -->
    <router-link to='/city'>
      <div class="header-right">
        城市
        <span class="iconfont" arrow-icon>&#xe619;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

 <!-- 1rem = html font-size = 50px -->
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .height-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
    .header-right
      width: 1.25rem
      margin-left: .1rem
      float: right
      text-align: centerds
      color: #fff
      .arrow-icon
        margin-left: -.0.8rem
        font-size: .24rem
</style>
