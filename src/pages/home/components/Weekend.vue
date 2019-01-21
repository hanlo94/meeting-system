<template>
  <div>
    <div class="recommend-tittle">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendLish" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgURL" />
        </div>
        <div class="item-info">
          <p class="item-title">{{item.tittle}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendLish: [{
        id: '001',
        imgURL: 'http://img1.qunarzz.com/sight/source/1505/d5/abe8a48a6ef8bf.jpg_r_640x214_7c41cc81.jpg',
        tittle: '武汉必打卡',
        desc: '到武汉感受神奇的热干面之都'
      },
      {
        id: '002',
        imgURL: 'http://img1.qunarzz.com/sight/source/1505/d5/abe8a48a6ef8bf.jpg_r_640x214_7c41cc81.jpg',
        tittle: '武汉必打卡',
        desc: '到武汉感受神奇的热干面之都'
      },
      {
        id: '003',
        imgURL: 'http://img1.qunarzz.com/sight/source/1505/d5/abe8a48a6ef8bf.jpg_r_640x214_7c41cc81.jpg',
        tittle: '武汉必打卡',
        desc: '到武汉感受神奇的热干面之都'
      }
      ]
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
  .item-img
    width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
    .item-desc
      line-height .4rem
      color #ccc
</style>
