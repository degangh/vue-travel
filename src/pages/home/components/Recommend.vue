<template>
  <div>
    <div class='recommendation-title'>Recommendation</div>
    <ul>
      
      <router-link  tag = "li"
      class='item border-bottom' 
      v-for='item of recommendList' 
      :key = 'item.id' 
      :to="'/detail/'+ item.id">
          <img class='item-img' :src = 'item.imgUrl' />
          <div class='item-info'>
            <p class='item-title'>{{item.title}}</p>
            <p class='item-desc'>{{item.desc}}</p>
            <button class='item-button'>View</button>
          </div>
      
      </router-link>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixin.styl'
  .recommendation-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent:  .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height:1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0px
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
      .item-button
        margin-top: .1rem
        line-height: .44rem
        background: #ff9300
        padding: 0.05rem 0.1rem
        border-radius: .06rem
        color: #fff
</style>
