<template>
    <div class="search">
        <input type="text" class="search-input" placeholder="Search destination">
    </div>
</template>

<script>
export default{
  name: 'CitySearch'
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
</style>
