<template>
  <div class="list">
    <ul>
      <li class="item" v-for="(item, key) in cities" :key="key">
        {{key}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Alphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .list
    display flex
    flex-direction column
    justify-content center
    position absolute
    top 1.58rem
    bottom 0
    right 0
    width .4rem
    .item
      line-height .34rem
      list-style-type:none
      text-align center
      color $bgColor
</style>
