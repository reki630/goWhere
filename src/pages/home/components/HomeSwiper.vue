<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwipper">
    <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <a href="https://touch.dujia.qunar.com/hotelpackages?tf=xbtj04&in_track=xbtj04" target="_blank">
          <img class="swiper-img" alt :src="item.imgUrl"/>
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
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      }
    }
  },
  computed: {
    showSwipper () {
      return this.swiperList.length
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
