<template class="home">
<div>
<home-header></home-header>

<home-carousel></home-carousel>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeCarousel from './components/Carousel'
export default {
  name: 'Home',
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper: HomeSwiper,
    HomeCarousel: HomeCarousel
  }
}
</script>

<style>

</style>
