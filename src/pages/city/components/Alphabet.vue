<template>
<div class='list'>
    <ul>
        <li class="item" 
        v-for = "(item) of letters" 
        :key = "item"
        :ref = "item.toUpperCase()"
        @click="handleLetterClick"
        @touchstart = "handleTouchStart"
        @touchmove = "handleTouchMove"
        @touchend = "handleTouchEnd"
        >{{item.toUpperCase()}}</li>
        
        
    </ul>

</div>

</template>

<script>
export default{
  name: 'CityAlphabet',
  props: {
      cities: Object
  },
  computed: {
      letters () {
          console.log(this.cities);
          const letters = []
          for (let i in this.cities) {
              letters.push(i)
              console.log(i)

          }
        return letters

      }
  },
  data () {
      return {
          touchStatus: false,
          startY: 0,
          timer: null
      }
  },

  updated () {
      this.startY = this.$refs['A'][0].offsetTop
  },
  methods: {
      handleLetterClick (e) {
          this.$emit('change', e.target.innerText)
      },

      handleTouchStart () {
          this.touchStatus = true
      },

      handleTouchMove (e) {
          if (this.touchStatus) {
              if (this.timer) {
                  clearTimeout(this.timer)
              }
              
            this.timer = setTimeout(() => {
            const touchY = e.touches[0].clientY - 79
            const index = Math.floor((touchY - this.startY) / 20)
            console.log(this.startY)
            if (index >= 0 && index < this.letters.length)
            this.$emit('change', this.letters[index].toUpperCase())
            },16)
              
          }

      },

      handleTouchEnd () {
          this.touchStatus = false
      }

  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variables.styl'
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    right: 0
    top: 1.3rem
    bottom: 0
    width: .4rem
    .item
        text-align:center
        line-height: .42rem
        color: $bgColor
  
</style>
