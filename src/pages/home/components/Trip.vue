<template>
  <div>
    <div class='title'>Trip</div>
    <ul>
      <li class='item border-bottom' v-for='item of tripList' :key = 'item.id'>
          <div class='item-img-wrapper'>
            <img class='item-img' :src = 'item.imgUrl' />
          </div>
          <div class='item-info'>
            <p class='item-title'>{{item.title}}</p>
            <p class='item-desc'>{{item.desc}}</p>
          </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  props: {
    tripList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixin.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent:  .2rem
  .item
    .item-img-wrapper
      height: 0
      padding-bottom: 33.9%
      overflow: hidden
    .item-img
      width: 100%
    .item-info
      padding: .1rem
      .item-title
        line-height: .54rem
        font-size: .32rem
        margin-bottom: 0px
        ellipsis()
      .item-desc
        line-height: .4 rem
        color: #ccc
        margin-bottom: 0px
        ellipsis()
</style>
