<template class="home">
<div>
<home-header></home-header>

<home-carousel></home-carousel>
<home-icons></home-icons>
<home-recommend></home-recommend>
<home-trip></home-trip>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeCarousel from './components/Carousel'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeTrip from './components/Trip'
export default {
  name: 'Home',
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper: HomeSwiper,
    HomeCarousel: HomeCarousel,
    HomeIcons: HomeIcons,
    HomeRecommend: HomeRecommend,
    HomeTrip: HomeTrip
  }
}
</script>

<style>

</style>
