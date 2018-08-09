<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201401/06/3fbbddda915cb7637439d484440d36be.jpg_600x330_0affc9e8.jpg">
      <div class="banner-info">
        <div class="banner-title">杭州乐园(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe6ee;</span>16</div>
      </div>
    </div>
    <common-gallary :imags="imags" v-show="showGallary" @close='handleGallaryClose'></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary.vue'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imags: ['http://img1.qunarzz.com/sight/p0/201401/06/3fbbddda915cb7637439d484440d36be.jpg_r_800x800_c7fa6286.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
.banner
  position :relative
  overflow :hidden
  height :0
  padding-bottom : 55%
  .banner-img
    width:100%
  .banner-info
    display :flex
    position :absolute
    left :0
    right :0
    bottom :0
    line-height :.6rem
    background-image :linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,.8))
    color :#fff
    .banner-title
      font-size :.32rem
      padding :0 .2rem
      flex:1
    .banner-number
      line-height :.32rem
      height :.32rem
      padding :0 .4rem
      margin-top :.14rem
      border-radius: .2rem
      background :rgba(0,0,0,.8)
      font-size :.24rem
      .banner-icon
        font-size :.24rem
</style>
