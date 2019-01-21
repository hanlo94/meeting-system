<template>
  <div>
    <div class="recommend-tittle">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendLish" :key="item.id">
          <img class="item-img" :src="item.imgURL" />
        <div class="item-info">
          <p class="item-title">{{item.tittle}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">景点详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      recommendLish: [{
        id: '001',
        imgURL: 'http://img1.qunarzz.com/sight/p0/201403/11/1f70100804193c28f8b71378c0faa49e.jpg_200x200_2b9d2349.jpg',
        tittle: '户部巷',
        desc: '户部，兵部，刑部，这些是古代政府机构'
      },
      {
        id: '002',
        imgURL: 'http://img1.qunarzz.com/sight/p0/201403/11/1f70100804193c28f8b71378c0faa49e.jpg_200x200_2b9d2349.jpg',
        tittle: '户部巷',
        desc: '户部，兵部，刑部，这些是古代政府机构'
      },
      {
        id: '003',
        imgURL: 'http://img1.qunarzz.com/sight/p0/201403/11/1f70100804193c28f8b71378c0faa49e.jpg_200x200_2b9d2349.jpg',
        tittle: '户部巷',
        desc: '户部，兵部，刑部，这些是古代政府机构'
      }]
    }
  }
}
</script>
<style lang='stylus' scoped>
  @import '~styles/mixins.styl'
  .recommend-tittle
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .16rem
        padding 0 .16rem
        background #ff9300
        border-radius .06rem
        color #fff
</style>
