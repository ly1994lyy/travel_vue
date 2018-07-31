<template>
  <div class="wraap">
    <swiper :options="swiperOption" v-if="shouSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class='swiper-img' :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  methods: {
    shouSwiper () {
      return this.list.length
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
