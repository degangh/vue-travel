<template class="home">
<div>
<home-header></home-header>

<home-carousel></home-carousel>
<home-icons></home-icons>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeCarousel from './components/Carousel'
import HomeIcons from './components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper: HomeSwiper,
    HomeCarousel: HomeCarousel,
    HomeIcons: HomeIcons
  }
}
</script>

<style>

</style>
