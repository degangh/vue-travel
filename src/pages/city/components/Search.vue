<template>
  <div>  
    <div class="search">
        <input type="text" class="search-input" v-model = "keyword" placeholder="Search destination">
    </div>
    <div class="search-content">
      <ul>
        <li v-for = "item in list" :key = "item.id">{{item.name}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
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
  
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
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
</style>
