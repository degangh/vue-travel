<template>
<div class='list' ref="wrapper">
    <div>
        <div class="area">
            <div class="title border-topbottom">Current Location</div>
            <div class="button-list">
                <div class="button-wrapper">
                    <div class="button">Adelaide</div>
                </div>
            </div>
        </div>

        <div class="area">
            <div class="title border-topbottom">Hot Places</div>
            <div class="button-list">
                <div v-for = "item of hotCities" :key = "item.id" class="button-wrapper">
                    <div class="button">{{item.name}}</div>
                </div>
                
            </div>
        </div>

        <div class="area" v-for = "(item, index) of cities" :key="index" :ref="index.toUpperCase()">
            <div class="title border-topbottom">{{index.toUpperCase()}}</div>
            <div class="item-list">
                <div class="item border-bottom" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</div>

            </div>
        </div>

        
    </div>
</div>

</template>

<script>
import Bscroll from 'better-scroll'
export default{
    props: {
        hotCities: Array,
        cities: Object,
        letter: String
    },
  name: 'CityList',
  mounted () {
      this.scroll = new Bscroll(this.$refs.wrapper)
  },
  watch: {
      letter() {
           
          if (this.letter)
          {
              const ele = this.$refs[this.letter][0]
              console.log(ele)
              this.scroll.scrollToElement(ele)
          }
      }
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variables.styl'
  .border-topbottom
    &:before
        border-color: #ccc
    &:after
        border-color: #ccc
  .border-bottom
    &:before
        border-color: #ccc
  .list
    overflow: hidden
    position: absolute 
    top: 1.58rem
    left: 0
    right: 0
    bottom:0
    .title
        line-height: .54rem
        padding-left .2rem
        background: #eee
        color: #666
        font-size: .26rem
    .button-list
        overflow: hidden
        padding: .1rem .6rem .1rem .1rem
        .button-wrapper
            float: left
            width: 33.3%
            .button
                padding: .1rem
                text-align: center
                margin: .1rem .1rem
                border: .02rem solid #ccc
                margin: .1rem
                border-radius: 0.06rem
    .item-list
        .item
            line-height: .76rem
            padding-left: .2rem
    

  
</style>
