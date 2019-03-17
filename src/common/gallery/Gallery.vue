<template>
<div class="container">
    <div class="wrapper">
        <a-carousel>
            <div ><img src="https://media-cdn.tripadvisor.com/media/attractions-splice-spp-540x360/06/90/de/bb.jpg" class="swiper-image"></div>
            <div ><img src="https://media-cdn.tripadvisor.com/media/photo-s/12/52/7b/34/small-group-bush-walk.jpg" class="swiper-image"></div>
        </a-carousel>
    </div>
</div>
</template>

<script>
  export default {
      name: "CommonGallery"
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
</style>