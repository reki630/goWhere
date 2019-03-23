<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
    <!-- slides -->
      <swiper-slide>
        <a href="https://touch.dujia.qunar.com/hotelpackages?tf=xbtj04&in_track=xbtj04" target="_blank">
          <img class="swiper-img" alt src="//img1.qunarzz.com/vc/bf/9d/a3/67b7b37511fa26a78298bf1da1.jpg"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a href="https://zt.dujia.qunar.com/bp/zt.php?id=4637&tf=xbtj02&in_track=xbtj02" target="_blank">
          <img class="swiper-img" alt src="//img1.qunarzz.com/vc/d3/79/22/687da305c0ea0532a2c7d3cc23.jpg"/>
        </a></swiper-slide>
      <swiper-slide>
        <a href="https://zt.dujia.qunar.com/bp/zt.php?id=4634&tf=xbtj03&in_track=xbtj03" target="_blank">
          <img class="swiper-img" alt src="//img1.qunarzz.com/vc/b8/25/51/f6173dbd12c1a0f783abe73855.jpg"/>
        </a>
      </swiper-slide>
      <swiper-slide>
        <a href="https://zt.dujia.qunar.com/bp/zt.php?id=4578&tf=xbtj05&in_track=xbtj05" target="_blank">
          <img class="swiper-img" alt src="//img1.qunarzz.com/vc/2a/96/76/d149c7a3a5b113f876f9a66e09.png"/>
        </a>
      </swiper-slide>
      <!-- Optional controls -->
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
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      }
    }
  }
}
</script>

<style lang='stylus' scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    width :100%
    height :0
    padding-bottom:31.25%
    overflow:hidden
    .swiper-img
      width :100%
</style>
