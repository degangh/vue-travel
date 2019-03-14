<template>
  <div>  
    <div class="search" >
        <input type="text" class="search-input" v-model = "keyword" placeholder="Search destination">
    </div>
    <div class="search-content" ref="search" v-show="keyword">
      <ul>
        <li 
        class="search-item border-bottom" 
        v-for = "item in list" 
        :key = "item.id"
        @click="handleCityClick(item.name)"
        >{{item.name}}</li>
        <li class="search-item border-bottom" v-show="hasNoData">No places found</li>
      </ul>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default{
  name: 'CitySearch',
  props: {
    cities: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.search)
  },

  computed: {
    hasNoData () {
      return !this.list.length 
    }
  },
  methods : {
    handleCityClick (city)
        {
            this.$store.dispatch('changeCity', city)
            this.$router.push('/')
        }
  },
  
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword){
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach((value) => {
            if (value.name.toLowerCase().indexOf(this.keyword.toLowerCase()) > -1 ) {
              result.push(value)
            } 
          })
        }
        this.list = result
      }, 100)
    }
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variables.styl'
  .search
    height: .72rem
    padding: 0 .1rem
    background: $bgColor
    .search-input
      height: .62rem
      line-height: .62rem
      width: 100%
      text-align: center
      border-radius: 2px
      color: #666
      box-sizing: border-box
      padding: 0 .1rem
  .search-content
    z-index: 1
    background:green
    overflow: hidden
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    background: #eee
    .search-item
      line-height: .62rem
      padding-left: .2rem
      color: #666
      background: #fff
</style>
