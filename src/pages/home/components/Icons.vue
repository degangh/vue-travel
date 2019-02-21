<template>
<div class= 'icons'>
    <a-carousel dots>
        <div v-for = "page of pages" :key='page.page'>
            <div class='icon' v-for = 'item of page' :key='item.id'>
                <div class='icon-content'>
                    <a-icon :type='item.type' class='icon-content-inner'/>
                </div>
                <p class='icon-desc'>{{item.desc}}</p>
            </div>

        </div>

    </a-carousel>
</div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },

  computed: {
    pages: function () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixin.styl'
.icons {
    margin-top: .05rem
    overflow: hidden
    height: 0
    padding-bottom: 40%

    .icon {
        position: relative
        display: inline-block
        width: 24%
        height: 0
        padding-bottom: 20%

        .icon-content {
            position: absolute
            top: 0
            left: 0
            right: 0
            bottom: 0.44rem
            box-sizing: border-box
            padding: 0.1rem

            .icon-content-inner {
                display: block
                margin: 0 auto
                height: 100%
                font-size: 0.6rem
                text-align: center
                color: #c0c0c0
            }
        }

        .icon-desc {
            position: absolute
            left: 0
            right: 0
            bottom: 0
            line-height: 0.44rem
            height: 0.44rem
            color: #333
            text-align: center
            ellipsis()
        }
    }
}

.icons >>> .slick-dots li .slick-active {
    background: #333
}

.icons >>> .slick-dots li button {
    background: #ccc
}
</style>
