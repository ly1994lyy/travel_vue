<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of list" :key="item.id">
      <div class="item-img-wrapper">
        <img :src="item.imgUrl" class="item-img">
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top :.3rem
  background :#eee
  line-height :.8rem
  text-indent :.2rem
.item-img-wrapper
  overflow :hidden
  height :0
  padding-bottom :33.4%
  .item-img
    width :100%
.item-info
  padding :.1rem
  .item-title
    ellipsis()
    line-height :.54rem
    font-size :.32rem
  .item-desc
    ellipsis()
    line-height :.4rem
    color :#ccc
</style>
