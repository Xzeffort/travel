<template>
   <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide v-for="item in swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imageUrl"/>
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
      swiperList: [{
        id: '001',
        imageUrl: 'http://img1.qunarzz.com/piao/fusion/1804/c4/1cdd28811593b802.jpg_750x200_5fbb7c91.jpg'
      }, {
        id: '002',
        imageUrl: 'http://img1.qunarzz.com/piao/fusion/1805/9e/f625886dec6c0402.jpg_750x200_417be630.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
      background #ffffff !important
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 26%
    background #ffffff
    .swiper-img
      width 100%
</style>
