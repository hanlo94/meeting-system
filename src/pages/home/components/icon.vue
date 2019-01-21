<template>
  <div class="icons">
    <swiper class="swiper-content">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-comtent" :src="item.imgURl" />
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
export default {
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      iconLish: [{
        id: '001',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '002',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '003',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '004',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '005',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '006',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '007',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '008',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      },
      {
        id: '009',
        imgURl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '旅游景点'
      }]
    }
  },
  computed: {
    // 用于pages页面轮播
    pages () {
      const pages = []
      this.iconLish.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .swiper >>> .swiper-pagination-bullet-active
    background #fff
  .icons >>> .swiper-content
    height 0
    padding-bottom 50%
  .icons
    margin-top .1rem
    .icon
      position relative
      float left
      overflow hidden
      width 25%
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-comtent
          display block
          margin 0 auto
          height 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align center
        color $darkTextColor
        ellipsis()
</style>
