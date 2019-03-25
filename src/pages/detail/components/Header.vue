<template>
<div>
    <router-link tag='div' to="/" class="header-abs" v-show="showAbs">
      <div class="header-abs-back"><a-icon type="left" /></div>
    </router-link>
    <div 
      class="header-fixed" 
      v-show="!showAbs"
      :style="opacityStyle"
    >
      <router-link to="/">
        <div class="header-fixed-back">
        <a-icon type="left" />
        </div>
        </router-link>
      Detail
    </div>
</div>
</template>

<script>

export default{
  name: 'DetailHeader',

  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop;
      if (top > 60 ) {
        let opacity = top/140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = {
          opacity
        }
        this.showAbs = false
      }
      else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll' , this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
    
}
</script>

<style lang = "stylus" scoped>
@import '~styles/variables.styl'
  .header-abs
    position: absolute
    left: .2 rem
    top: .2rem
    width: .8rem
    height: .8rem
    line-height: .8rem
    border-radius: .4rem
    background: rgba(0, 0, 0, .8)
    .header-abs-back
      font-size: .5rem
      padding-left: .1rem
      color: #fff
  .header-fixed
    position:fixed
    top: 0
    left: 0
    right: 0
    overflow: hidden
    line-height: $headerHeight
    height: $headerHeight
    text-align: center
    color: #fff
    background: $bgColor
    font-size: .32rem
    .header-fixed-back
      width: .64rem
      text-align: center
      font-size: .4rem
      position: absolute
      top: 0
      left: 0
      color: #fff;

</style>
