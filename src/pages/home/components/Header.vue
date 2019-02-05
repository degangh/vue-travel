<template class="home">
<div class="header">
<div class="header-left"><div class="back-icon"><a-icon type="left" /></div></div>
<div class="header-input"> <a-icon type="search" /> Search Keyword</div>
<div class="header-right">City <div class="arrow-icon"><a-icon type="caret-down" /></div></div>
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
        .back-icon
            text-align: center
            font-size: .4rem

    .header-input
        flex: 1
        height: .64rem
        line-height: .64rem
        margin-top: .12rem
        margin-left: .2rem
        background: #fff
        border-radius: .1rem
        color: #ccc
        padding-left: .1rem

    .header-right
        text-align: center
        width: 1.24rem
        float: right
        .arrow-icon
            font-size: .2rem
            display:inline-block


</style>
