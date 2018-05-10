<template>
  <div class="header">
      <div class="header-left">
          <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
          <span class="iconfont">&#xe632;</span>
          输入城市/景点/游玩/主题
          </div>
      <div class="header-right">
          {{this.city}}
          <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display flex
        line-height  .86 rem
        background $bgColor
        color #fff
        .header-left
            width .64 rem
            float left
            .back-icon
                text-align center
                font-size .4 rem
        .header-input
            flex 1
            height .64 rem
            line-height .64 rem
            margin-top .12 rem
            margin-left .2 rem
            padding-left .2 rem
            background #fff
            border-radius .1 rem
            color #cccccc
        .header-right
            width 1.24 rem
            float right
            text-align center
            .arrow-icon
                font-size .24 rem;
</style>
