<template>
  <div>
    <div class="homeWeekend-title">周末去哪儿</div>
    <ul>
      <li class="homeWeekend-item border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl' alt/>
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
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .homeWeekend-title
    line-height :.8rem
    background: #eeeeee
    text-indent: .2rem
  .item-img-wrapper
    overflow :hidden
    height :0
    padding-bottom :37%
    .item-img
      width :100%
  .item-info
    padding:.2rem
    .item-title
      line-height :.5rem
      font-size:.3rem
      ellipsis()
    .item-desc
      line-height :.4rem
      color:#ccc
      ellipsis()
</style>
