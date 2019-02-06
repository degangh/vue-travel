<template>
<div class="wrapper">
<swiper :options="swiperOption" >
    <!-- slides -->
    <swiper-slide>
        <img class= "swiper-image" src = 'https://media-cdn.tripadvisor.com/media/photo-f/05/47/e4/65/bird-tours-sa-private.jpg' />
    </swiper-slide>
    <swiper-slide>
        <img class= "swiper-image" src = 'https://media-cdn.tripadvisor.com/media/photo-s/0d/f4/fe/a1/2-day-kangaroo-island.jpg' />
    </swiper-slide>

    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>

</swiper>
</div>
</template>

<script>
export default{
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper
        width: 100%
        height: 40vw
        .swiper-image
            width: 100%
</style>
