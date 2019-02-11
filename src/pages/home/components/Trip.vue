<template>
  <div>
    <div class='title'>Trip</div>
    <ul>
      <li class='item border-bottom' v-for='item of recommendList' :key = 'item.id'>
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
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/15/cb/81/98/barossa-valley-day-trip.jpg',
          title: 'Waterfall Gully',
          desc: 'Waterfall Gully is an eastern suburb of the South Australian capital city of Adelaide. It is located in the foothills of the Mount Lofty Ranges around 5 km (3.1 mi) east-south-east of the Adelaide city centre.'
        },
        {
          id: '0002',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/0d/f4/fe/9c/kangaroo-island-in-a.jpg',
          title: 'Waterfall Gully',
          desc: 'Waterfall Gully is an eastern suburb of the South Australian capital city of Adelaide. It is located in the foothills of the Mount Lofty Ranges around 5 km (3.1 mi) east-south-east of the Adelaide city centre.'
        },
        {
          id: '0003',
          imgUrl: 'https://media-cdn.tripadvisor.com/media/photo-s/16/00/15/15/adelaide-highlights-and.jpg',
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
