<template>
<div class='list'>
    <div class="area">
        <div class="title border-topbottom">Current Location</div>
        <div class="button-list">
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
        </div>
    </div>

    <div class="area">
        <div class="title border-topbottom">Hot Places</div>
        <div class="button-list">
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
            <div class="button-wrapper">
                <div class="button">Adelaide</div>
            </div>
        </div>
    </div>

    <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>

        <div class="title border-topbottom">A</div>
        <div class="item-list">
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
            <div class="item border-bottom">Adelaide</div>
        </div>
    </div>
  
</div>

</template>

<script>
export default{
  name: 'CityList'
}
</script>

<style lang='stylus' scoped>
  @import '~styles/variables.styl'
  .border-topbottom
    &:before
        border-color: #ccc
    &:after
        border-color: #ccc
  .border-bottom
    &:before
        border-color: #ccc
  .list
    overflow: hidden
    position: absolute 
    top: 1.58rem
    left: 0
    right: 0
    bottom:0
    .title
        line-height: .4rem
        padding-left .2rem
        background: #eee
        color: #666
        font-size: .26rem
    .button-list
        overflow: hidden
        padding: .1rem .6rem .1rem .1rem
        .button-wrapper
            float: left
            width: 33.3%
            .button
                padding: .1rem
                text-align: center
                margin: .1rem .1rem
                border: .02rem solid #ccc
                margin: .1rem
                border-radius: 0.06rem
    .item-list
        .item
            line-height: .76rem
            padding-left: .2rem
    

  
</style>
