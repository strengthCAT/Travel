<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_600x330_4ae7abf5.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          深圳小梅沙海洋世界
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe663;</span>
          16
        </div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      imgs: ['//img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_600x330_4ae7abf5.jpg',
        'http://img1.qunarzz.com/sight/p0/201301/05/4487433de3574f7f93835fbb.png_r_800x800_6ce7545e.png'],
      showGallary: false
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position relative
  overflow hidden
  height 0
  padding-bottom 55%
  .banner-img
    width 100%
  .banner-info
    display flex
    position absolute
    left 0
    right 0
    bottom 0
    line-height .6rem
    color #fff
    background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
    .banner-title
      flex 1
      font-size .32rem
      padding .2rem
    .banner-number
      height .32rem
      line-height .32rem
      padding 0 .4rem
      margin-top .14rem
      border-radius .2rem
      background rgba(0, 0, 0, .8)
      font-size .24rem
      .banner-icon
        font-size .24rem
</style>
