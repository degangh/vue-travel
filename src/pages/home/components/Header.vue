<template class="home">
<div class="header">
<div class="header-left">Back</div>
<div class="header-input">Search Keyword</div>
<div class="header-right">City</div>
</div>
</template>

<script>

export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus"  scoped>
.header
    display: flex
    line-height: .86rem
    background: #00bcd4
    color: #fff

    .header-left
        width: .64rem
        float: left

    .header-input
        flex: 1
        height: .64rem
        line-height: .64rem
        margin-top: .12rem
        margin-left: .2rem
        background: #fff
        border-radius: .1rem
        color: #ccc

    .header-right
        text-align: center
        width: 1.24rem
        float: right

</style>
