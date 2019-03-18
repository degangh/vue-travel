<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img src="https://media-cdn.tripadvisor.com/media/attractions-splice-spp-540x360/06/90/de/bb.jpg" class="banner-img"/>    
        <div class="banner-info">
            <div class="banner-title"> Lion 360 Experiences</div>
            <div class="banner-number"><a-icon type="picture" /> {{imgs.length}}</div>
        </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallery" @closeGallery="handleGalleryClose"></common-gallery>
</div>
</template>

<script>
import CommonGallery from 'common/gallery/gallery'
export default{
    name: 'DetailBanner',
    components: {
        CommonGallery
    },
    data () {
        return {
            showGallery: false,
            imgs: [
             "https://media-cdn.tripadvisor.com/media/attractions-splice-spp-540x360/06/90/de/bb.jpg",
             "https://media-cdn.tripadvisor.com/media/photo-s/12/52/7b/34/small-group-bush-walk.jpg",
             "https://media-cdn.tripadvisor.com/media/photo-s/16/23/34/93/giraffe-safari-and-a.jpg"
            ]
        }
    },
    methods: {
        handleBannerClick () {
            this.showGallery = true
        },

        handleGalleryClose () {
            this.showGallery = false
        }
    }
}
</script>

<style lang = "stylus" scoped>
  .banner
    position: relative
    height: 0
    padding-bottom: 67%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .6 rem
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      color: #fff
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        margin-top: .14rem   
        padding:0 .4rem 
        line-height: .32rem  
        height: .32rem
        border-radius .2rem
        font-size: .24rem
        background: rgba(0,0,0, .8)
</style>