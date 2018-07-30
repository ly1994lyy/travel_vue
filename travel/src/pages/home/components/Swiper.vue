<template>
  <div class="wraap">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class='swiper-img' :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {id: '0001', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1807/ec/278a34afb59a0d02.jpg_750x200_3292a705.jpg'},
        {id: '0002', imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/3c/c72a1ccd4d7b2202.jpg_750x200_b88bbab4.jpg'}
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wraap >>> .swiper-pagination-bullet-active
    background :#fff !important
.wraap
  width :100%
  overflow :hidden
  height :0
  padding-bottom :30.5%
  .swiper-img
    width :100%
</style>
