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
  data () {
    return {
      iconList: [
        {
          id: '0001',
          type: 'car',
          desc: 'Car Rental'
        },
        {
          id: '0002',
          type: 'coffee',
          desc: 'Cafe'
        },
        {
          id: '0003',
          type: 'shop',
          desc: 'Restaurant'
        },
        {
          id: '0004',
          type: 'wallet',
          desc: 'Money'
        },
        {
          id: '0005',
          type: 'phone',
          desc: 'Helpline'
        },
        {
          id: '0006',
          type: 'shopping',
          desc: 'Shopping'
        },
        {
          id: '0007',
          type: 'home',
          desc: 'Hotel'
        },
        {
          id: '0008',
          type: 'camera',
          desc: 'Place to go'
        },
        {
          id: '0009',
          type: 'wifi',
          desc: 'Internet'
        }
      ]
    }
  },

  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })

      console.log(pages)
      return pages
    }
  }
}
</script>

<style lang='stylus' scoped>
@import '~styles/mixin.styl'
.icons {
    overflow: hidden
    height: 0
    padding-bottom: 50%

    .icon {
        position: relative
        display: inline-block
        width: 24%
        height: 0
        padding-bottom: 25%

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
                font-size: 0.8rem
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
