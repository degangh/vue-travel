<template class="home">
<div>
<home-header :city="data.city"></home-header>

<home-carousel :carouselList = "data.carouselList"></home-carousel>
<home-icons :list = "iconList" ></home-icons>
<home-recommend :recommendList = "data.recommendList"></home-recommend>
<home-trip :tripList = "data.tripList"></home-trip>
</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeCarousel from './components/Carousel'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeTrip from './components/Trip'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader: HomeHeader,
    HomeCarousel: HomeCarousel,
    HomeIcons: HomeIcons,
    HomeRecommend: HomeRecommend,
    HomeTrip: HomeTrip
  },

  mounted () {
    this.getHomeInfo()
  },

  data () {
    return {
      data: {},
      iconList: []
    }
  },

  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSuccess)
    },

    getHomeInfoSuccess (res) {
      this.data = res.data.data
      this.iconList = this.data.iconList // ?why
    }
  }
}
</script>

<style>

</style>
