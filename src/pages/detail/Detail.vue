<template>
<div>
<detail-banner
    :sightName="sightName"
    :bannerImg="bannerImg"
    :bannerImgs="galleryImgs"
    ></detail-banner>
<detail-header></detail-header>
<div class='content'>
    <detail-list :list = "list"></detail-list>
</div>
</div>
</template>

<script>
import DetailBanner from './components/Banner.vue'
import DetailHeader from './components/Header.vue'
import DetailList from './components/List.vue'
import axios from 'axios'
export default {
    name: 'Detail',
    components: {
        DetailBanner,
        DetailHeader,
        DetailList
    },
    methods: {
        getDetailInfo() {
            console.log('get info')
            axios.get('/api/detail.json' , {
                params: {
                    id: this.$route.params.id
                }
            }).then(this.getDetailDataSucc)
        }, 

        getDetailDataSucc (res) {
            console.log(res.data)
            res = res.data
            if (res.ret && res.data) {
                const data = res.data
                this.sightName = data.sightName
                console.log(data.sightName)
                this.bannerImg = data.bannerImg
                this.galleryImgs = data.galleryImgs
                this.list = data.categoryList
            }
        }
    },
    activated () {
        this.getDetailInfo()
    },
    data () {
        return {
            sightName: '',
            bannerImg: '',
            galleryImgs: [],
            list: []
        }
    }
}
</script>

<style scoped lang="stylus">
  .content
    height: 50rem
</style>
