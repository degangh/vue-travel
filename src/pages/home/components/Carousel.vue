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
  props: {
    carouselList: Array
  }
}
</script>

<style lang="stylus" scoped>
.wrapper {
  width: 100%;
  height: 50vw;
  .swiper-image {
    width: 100%;
    height: 50vw;
    object-fit: cover
  }
.wrapper >>> .ant-carousel .slick-dots {
  bottom: 1.2rem !important
}

}
</style>
