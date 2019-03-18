<template>
<div class="container" @click="handleGalleryClick">
    <div class="wrapper">
        <a-carousel>
            <div v-for = "(img, index) in imgs" :key = "index"><img :src="img" class="swiper-image"></div>
            
        </a-carousel>
    </div>
</div>
</template>

<script>
  export default {
      name: "CommonGallery",
      props: {
        imgs: {
            type: Array,
            default () {
            return []
        }
      }
     },
     methods: {
         handleGalleryClick () {
             this.$emit('closeGallery')
         }
     }
  }
</script>

<style lang="stylus" scoped>
  .container
    display: flex
    flex-direction: column
    justify-content: center
    position: fixed
    left: 0
    right: 0
    top: 0
    bottom: 0
    background: #000
    z-index: 99
    .wrapper
      background: #fff
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 90%
    .wrapper >>> .ant-carousel .slick-dots
      bottom: 1.2rem !important
</style>