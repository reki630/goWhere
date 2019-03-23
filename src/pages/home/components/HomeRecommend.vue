<template>
  <div>
    <div class="homeRecommend-title">热销推荐</div>
    <ul>
      <li class="homeRecommend-item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src='item.imgUrl' alt/>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .homeRecommend-title
    margin-top:.2rem
    line-height :.8rem
    background: #eeeeee
    text-indent: .2rem
  .homeRecommend-item
    display :flex
    height :1.9rem
    overflow :hidden
    .item-img
      width :1.7rem
      height :1.7rem
      padding:.1rem
    .item-info
      flex :1
      padding:.1rem
      min-width:0
      .item-title
        line-height :.5rem
        font-size:.3rem
        ellipsis()
      .item-desc
        line-height :.4rem
        color:#ccc
        ellipsis()
      .item-button
        background :#ff9300
        line-height:.5rem
        margin-top:.1rem
        padding:0 .2rem
        border-radius:.06rem
        color:#fff
</style>
