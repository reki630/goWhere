<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont back-home">&#xe624;</div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position :relative
    height :$headerHeight
    line-height :$headerHeight
    overflow :hidden
    text-align :center
    color:#fff
    background :$bgColor
    font-size :.32rem
    .back-home
      position :absolute
      top :0
      left :0
      width :.64rem
      text-aligh:center
      font-size :.4rem
      color :#fff
</style>
