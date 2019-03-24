<template>
  <div class="gallary-container" @click="handleGallaryClose">
    <div class="wrapper">
      <swiper :options="swiperOption">
      <!-- slides -->
        <swiper-slide  v-for="(item,index) in gallaryImgs" :key="index">
            <img class="swiper-img" alt :src="item"/>
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Gallary',
  props: {
    gallaryImgs: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        observer: true,
        observeParents: true
      }
    }
  },
  methods: {
    handleGallaryClose () {
      this.$emit('close')
    }
  }
}
</script>

<style lang='stylus' scoped>
  .gallary-container >>> .swiper-container
    overflow:inherit
  .gallary-container
    position: fixed
    display :flex
    flex-direction :column
    justify-content :center
    left :0
    right :0
    top:0
    bottom:0
    background :#000
    z-index :99
    .wrapper
      height :0
      width :100%
      padding-bottom:100%
      .swiper-img
        width :100%
      .swiper-pagination
        color:#fff
        bottom:-1rem
</style>
