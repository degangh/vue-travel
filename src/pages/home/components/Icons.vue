<template>
<div class= "icons">
    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>

    <div class="icon">
        <div class="icon-content">
            <a-icon type="dollar" class="icon-content-inner"/>
        </div>
        <p class="icon-desc">Logo</p>    
    </div>



</div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data() {
        return {}
    }
}
</script>

<style lang="stylus" scoped>
    .icons
        overflow hidden
        
        height: 0
        padding-bottom: 50%

        .icon
            position: relative
            display:inline-block
            width:24%
            height: 0
            padding-bottom:25%

            .icon-content
                position: absolute
                top:0
                left:0
                right:0
                bottom: .44rem
                box-sizing: border-box
                padding: .1rem
                .icon-content-inner
                    display:block
                    margin: 0 auto
                    height:100%
                    font-size: .8rem
                    text-align:center
                    color: #c0c0c0

            .icon-desc
                position: absolute
                left: 0
                right: 0
                bottom: 0
                line-height: .44rem
                height: .44rem
                color: #333
                text-align:center
                    

                    


                
</style>