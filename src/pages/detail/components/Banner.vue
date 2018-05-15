<template>
    <div>
      <div class="banner" @click="handleBannerClick">
        <img class="banner-img" :src="bannerImg">
        <div class="banner-info">
          <div class="banner-title">{{sightName}}</div>
          <div class="banner-number">
            <span class="iconfont banner-icon">&#xe653;</span>{{bannerImgs.length}}
          </div>
        </div>
      </div>
      <gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></gallary>
    </div>
</template>

<script>
import Gallary from 'common/gallary/Gallary'
export default {
  name: 'Banner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/wugc/p3/201206/02/44c1fe10b91aed6793835fbb.jpg_r_800x800_8c63be46.jpg',
        'http://img1.qunarzz.com/wugc/p3/201206/02/44c1fe10b91aed6793835fbb.jpg_r_800x800_8c63be46.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    Gallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #ffffff
      background-image linear-gradient(top, rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        height .32rem
        margin-top .14rem
        padding 0 .4rem
        line-height .32rem
        border-radius .2rem
        background rgba(0,0,0,.8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
