<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      <span>输入城市景点/游玩/主题</span>
      </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>
<script>
export default {
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      text-align: center
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      color: #ccc
      margin-top: .12rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
    .header-right
      width: 1.24rem
      float: right
      text-align: center
</style>
