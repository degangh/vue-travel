<template>
<div class='list'>
    <ul>
        <li class="item" v-for = "(item , index) of cities" :key = "index">{{index.toUpperCase()}}</li>
        
        
    </ul>

</div>

</template>

<script>
export default{
  name: 'CityAlphabet',
  props: {
      cities: Object
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
