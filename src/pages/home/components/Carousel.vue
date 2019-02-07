<template>
<div class="wrapper">
  <a-carousel autoplay>
    <div v-for = "(item,index) in carouselList" :key="index"><img :src="item.imgUrl" class="swiper-image"></div>
  </a-carousel>
</div>
</template>

<script>
export default {
  name: 'HomeCarousel',
  data () {
    return {
      carouselList: [
        {
          id: '001',
          imgUrl:
            'https://media-cdn.tripadvisor.com/media/photo-f/05/47/e4/65/bird-tours-sa-private.jpg'
        },
        {
          id: '002',
          imgUrl:
            'https://media-cdn.tripadvisor.com/media/photo-s/0d/f4/fe/a1/2-day-kangaroo-island.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper {
  overflow hidden;
  width: 100%;
  height: 60vw;

  .swiper-image {
    width: 100%;
  }
}
</style>
