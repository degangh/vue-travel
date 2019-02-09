<template>
  <div>
    <div class='recommendation-title'>Recommendation</div>
    <ul>
      <li class='item border-bottom' v-for='item of recommendList' :key = 'item.id'>
          <img class='item-img' :src = 'item.imgUrl' />
          <div class='item-info'>
            <p class='item-title'>{{item.title}}</p>
            <p class='item-desc'>{{item.desc}}</p>
            <button class='item-button'>View</button>
          </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/03/69/49/6a/waterfall-gully-to-mount.jpg',
          title: 'Waterfall Gully',
          desc: 'Waterfall Gully is an eastern suburb of the South Australian capital city of Adelaide. It is located in the foothills of the Mount Lofty Ranges around 5 km (3.1 mi) east-south-east of the Adelaide city centre.'
        },
        {
          id: '0002',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/03/69/49/6a/waterfall-gully-to-mount.jpg',
          title: 'Waterfall Gully',
          desc: 'Waterfall Gully is an eastern suburb of the South Australian capital city of Adelaide. It is located in the foothills of the Mount Lofty Ranges around 5 km (3.1 mi) east-south-east of the Adelaide city centre.'
        },
        {
          id: '0003',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/03/69/49/6a/waterfall-gully-to-mount.jpg',
          title: 'Waterfall Gully',
          desc: 'Waterfall Gully is an eastern suburb of the South Australian capital city of Adelaide. It is located in the foothills of the Mount Lofty Ranges around 5 km (3.1 mi) east-south-east of the Adelaide city centre.'
        }
      ]
    }
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
